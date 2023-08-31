### CMakeGitCloneMinimal
* clone git repository with init,fetch and checkout.
* save the reusult using short hash.

### example
```cmake
include(CMakeExecuteGit.cmake)
CMakeGitCloneMinimal( test_repo 
        #FORCE_UPDATE 
        REPOSITORY_NAME test_repo 
        REPOSITORY_REMOTE origin  
        REPOSITORY_URI path_to_test_repo  
        DESTINATION ${CMAKE_CURRENT_SOURCE_DIR}/third_party/cmake
        HASH 187df80840a8f1a03f05867ff9e5c55fc4614b7c # specify HASH, TAG or Branch
        #TAG v0.0.2
        #BRANCH master
        #VERBOSE 
        #VERBOSE_GIT
        )
message(${test_repo}) # path to repository
```