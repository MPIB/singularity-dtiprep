# singularity-dtiprep
Singularity recipes for base-images containing DTIPrep.

 - DTIPrep is pulled from its [github repository](https://github.com/NIRALUser/DTIPrep) and build using cmake.
 - cmake and the build dependencies are installed through the debian repositories via `apt-get install`.
 - At the end of the build process the image is cleaned up by:
    - removing cmake and build dependencies through `apt-get purge`,
    - deleting the package cache,
    - deleting the folder containing the cloned repository.