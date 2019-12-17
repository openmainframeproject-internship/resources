#  Build dockerHub development stacks

## Description

This project will produce a suite of Docker images for OpenSUSE and ClefOS (a CentOS clone for Z).

If you go to Dockerhub and look at  https://hub.docker.com/u/clefos you’ll see all the existing builds for Z. These are all based on a CentOS clone called ClefOS. The source for most of these (excluding the OpenShift and Source-to-Image images) may be found at https://github.com/nealef/docker. 

What we want to do is:

* Keep these images current. In many cases the recipes were created on existing CentOS images and others were created by me. I would like a mechanism for keeping both the derived and original recipe kept current and the dockerhub repo updated more regularly.
* Where possible produce the equivalent suite based on OpenSUSE. It’s possible that some packages used for ClefOS images may not exist for OpenSUSE. Part of this project will be to document the deficiencies.
* In addition the are  many of the images for created based on the OpenShift Origin software collection. These recipes are found at:https://github.com/nealef/okcd-images.git. A mechanism to keep these up to date is desired. The okcd-images repo shows the type of model I’d like to apply to the other repo as well (if possible – it won’t always be possible). That is, we pull from the seminal repo, apply any s390x-specific fixes if required, and build from there. Many times the fix is to change the FROM image name to a ClefOS one.

In most instances all these images are updated on an ad-hoc basis. I would like something like this: create a PR on github that will trigger a build and ultimately a push of the image to dockerhub. This would entail creating a CI mechanism (like Jenkins) to properly automate and manage the process.

Some of the builds have test suites others don’t. If a test suite could be developed for all or most of these images then this would be a bonus.

## Additional Information

Open source projects known working on s390 listed at https://www.ibm.com/developerworks/community/forums/html/topic?id=5dee144a-7c64-4bfe-884f-751d6308dbdf

## Desirable Skills

Basic Linux devops

## Expected Outcome

DockerHub images for s390x

## Difficultly

*Medium*

## Mentors

* Neale Ferguson <neale@sinenomine.net>
