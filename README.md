# Test CI placeholder demo

In this repository you can find a workflow that shows a placeholder implementation of how a deployment and integration etc test pipeline would look for each of our component repositories.

The general idea is 
-   trigger on pr and merge to main
-   run a container with latest release already deployed on it
-   copy the repo of the component to be tested into the already deployed riflex release repository inside the container
-   run neccesary build steps on the newly copied repo, colcon build, git lfs? etc
-   perform deployment test
-   if deployment test succesful -> perform intergration and regression test
-   if all are succesful -> build the new release and push it
