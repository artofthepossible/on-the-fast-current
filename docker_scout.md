### Using Docker Scout Lab

Time to Complete: 15-20 minutes

1. To get started with Docker Build Scout, you need to:
a. Activate Docker Scout on at least one repository

### Overview
Docker Scout enhances container security by providing automated vulnerability detection and remediation, addressing insecure container images, and ensuring compliance with security standards.
It Works well with Docker Desktop, GitHub Actions, Jenkins, Kubernetes, and other CI solutions.
[Software supply chain security] (https://youtu.be/YzNK6E7APv0)
[Software Bill Of Materials] (https://youtu.be/PbS4y7C7h4A)

Building a secure software supply chain involves several key steps, such as:

Identify the software components and dependencies you use to build and run your applications.
Automate security testing throughout the software development lifecycle.
Monitor your software supply chain for security threats.
Implement security policies that govern how software is built, and the components it contains.

### Part 1: Enable Docker Scout
1. Activate Docker Scout on atleast one repository
   ```sh 
   https://scout.docker.com/org/demonstrationorg/settings/repos
   ```
   or via cli 

   ```sh 
    docker scout repo enable --org ORG_NAME ORG_NAME/scout-demo
    docker scout repo enable --org demonstrationorg demonstrationorg/bank-demo-whale-of-a-time

   ```
2. Setup docker desktop settings
    Enable image SBOM indexing.
    Enable background SBOM indexing

2. What's next:
    Manage repositories in the Docker Scout Dashboard → https://scout.docker.com/org/demonstrationorg/settings/repos

2b. View build details: docker-desktop://dashboard/build/desktop-linux/desktop-linux/8uqkz6tp5s4untuv662hbf3eh

3. To view the same output via the cli
To view the summary of image vulnerabilities and recommendations, we run the first command listed here

    ```sh 
    docker scout quickview 
    ```

4. To  View vulnerabilities, we run the second command docker scout cves
    ```sh 
    docker scout cves 
    ```

5. To view the docker scout recommendations, , we run the third command to compare and contrast the image across two builds,  
    ```sh 
    docker scout recommendations
    ```

6. Navigate to the images tab, we see the image hierarchy if we select our image 
Here you can see we have a number of high, medium and low vulnerabilities at the image level all the way down to the individual packages
As a developer, NOW We focus our attention on how we can fix our application
We have a recommendations fixes tab here, that allows the developer to get some guidance on how resolve these vulnerabilities
Under change base image, we can view the the base image options available and how vulnerabilities are affected from the old image to recommended image

6. To fix missing supply chain attestations
    docker build --push --sbom=true --provenance=true -t demonstrationorg/bank-demo-whale-of-a-time:v1 .

### Part 4: Health Scores - Docker Desktop:

1. To view the health score of an image in Docker Desktop:

    a. Open Docker Desktop and sign in to your Docker account. </br>
    b. Navigate to the Images view and select the Hub tab.</br>
    c. In the list of repositories, the Health column displays the scores of the different tags that have been pushed to Docker Hub.</br>

    The health score badge is color-coded to indicate the overall health of the repository: </br>

    Green: A score of A or B.</br>
    Yellow: A score of C.</br>
    Orange: A score of D.</br>
    Red: A score of E or F.</br>
    Gray: An N/A score.</br>

### Part 5: Health Scores - Docker Hub:
1. To view the health score of an image in Docker Hub: </br>

2. Go to Docker Hub and sign in. </br>
3. Navigate to your organization's page. </br>
4. In the list of repositories, you can see the health score of each repository based on the latest pushed tag. </br>



### Part 6: Health Scores - Improving your health score
To improve the health score of an image, take steps to ensure that the image is compliant with the Docker Scout recommended policies. </br>

1. Go to the Docker Scout Dashboard. </br>
2. Sign in using your Docker ID. </br>
3. Go to Repository settings and enable Docker Scout for your Docker Hub image repositories. </br>
4. Analyze the policy compliance for your repositories, and take actions to ensure your images are policy-compliant. </br>
Since policies are weighted differently, prioritize the policies with the highest scores for a greater impact on your image's overall score. </br>
a. In Docker Desktop, select View in Hub
b. In Docker Hub, select [view in Docker Scout Dashboard](https://scout.docker.com/reports/org/demonstrationorg/images/host/hub.docker.com/repo/demonstrationorg%2Fwhale-of-a-time-scout-demo/tag/v3/digest/sha256%3A1ac649615092d9e30ff4d6c10ad84733d5212451e406b9a331143c1208f18ff4?utm_source=hub&utm_medium=actions-button&_gl=1*1kj2f6f*_gcl_aw*R0NMLjE3MzA3NjQyMDkuQ2owS0NRaUFfcUc1QmhEVEFSSXNBQTBVSFNLZ2NEcUJJenQ3a1JfaktfSmoyR1JBaC1heHd4QlJaQmpaMEc3TUlmand6STNPUktqVDhUUWFBbVdjRUFMd193Y0I.*_gcl_au*MTQxNjYwMDAzNC4xNzMzNzczMTAy*_ga*ODQyNDk2NzMyLjE3MDI0MDA3MjY.*_ga_XJWPQMJYHQ*MTczNjE4NjcxNy4xNTg1LjEuMTczNjE4OTQ5OC42MC4wLjA.)
c. Under [Policy Status](https://scout.docker.com/reports/org/demonstrationorg/images/host/hub.docker.com/repo/demonstrationorg%2Fwhale-of-a-time-scout-demo/tag/v3/digest/sha256%3A1ac649615092d9e30ff4d6c10ad84733d5212451e406b9a331143c1208f18ff4/policy)

### Part 6: Docker Scout:Building images with provenance and SBOMs
d. For example, To Fix - Missing supply chain attestation(s), Rebuild the image with a new tag and push it to your Docker Hub repository:

    ```sh 
    docker build --push --sbom=true --provenance=true -t demonstrationorg/whale-of-a-time-scout-demo:v4 .



    ```

### Part 7:  View in Dashboard
1. After pushing the updated image with attestations, it's time to view the results through a different lens: the Docker Scout Dashboard.

2. Open the Docker Scout Dashboard.
3. Sign in with your Docker account.
4. Select Images in the left-hand navigation.
5. Review the newly rebuilt image and corresponding healthscore via the docker scout dashboard
    ```sh
    https://scout.docker.com/reports/org/demonstrationorg/images/host/hub.docker.com/repo/demonstrationorg%2Fwhale-of-a-time-scout-demo/tag/v4/digest/sha256%3A1ac649615092d9e30ff4d6c10ad84733d5212451e406b9a331143c1208f18ff4/policy
    ```