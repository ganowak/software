## Difference 

-  `lb-dev` does not modify the runtime environment and does not call cd to switch to the created directory.
-   the default version of a project used by `lb-dev` is prod, instead of picking up the latest one.
-   `lb-dev` supports CMake-based LHCb software projects while `SetupProject` does not.
-   by default `SetupProject` creates the local project in `$User_release_area`, while `lb-dev` creates it in the current (or specified) directory 

 `SetupProject` is no longer working and really all the old documentation needs update :(
 
 `SetupProject DaVinci v45r8` = `lb-run DaVinci/v45r8 $SHELL` but this unsupported anyway. 
 
 ## References 
 [ Tools for the LHCb Software Environment](https://twiki.cern.ch/twiki/bin/view/LHCb/SoftwareEnvTools#Comparison_with_SetupProject)
