# How did you test your pipeline?

I created the Jenkinsfile for the pipeline in VS Code for IDE validation. With the help of an extension, I was able to validate syntax issues. For end-to-end testing, I created a sandbox job to verify if the script works as expected.

# How did you test your repo?

I used `unittest` to verify my logparser script. Additionally, I ran the script first with a test sample logfile and then with a generated logfile to verify if it works as expected.

# Since repoA contains binaries, what is the advantage of using LFS?

It helps reduce size of your repository as the binaries will be stored outside of repository(LFS storage system) as LFS objects. GIT LFS replaces large files in the repository with a pointer file.

# How to adjust this repository to support LFS?

 First is to identify large binaries or files that are not necessarily required to be  added in the repository. These are binaries or files that are auto-generated or can be re-generated.
 After identifying the necessary binaries/ files that are need to be in the repository, we cam add it to Git LFS tracking.
 After migrating the identified large files, we can commit and push changes. It is also good to check if the files that are added to LFS tracking are documented properly (commit message can do) for transparency with other collaborators

