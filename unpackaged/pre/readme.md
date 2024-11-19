This directory should contain metadata which you intend to deploy after the main deployment. If you want to add metadata to this directory, add a subdirectory for each grouping of metadata you want to deploy and if needed add a numerical value to start of the directory name to ensure that metadata is deployed in a certain order.

For example:

unpackaged / pre
                 / 1_Profiles
                      /profiles
                          Admin.profile-meta.xml
                          ...
                 / 2_CustomObjects
                      /objects
                          MyCustomObject__c
                              fields
                              ...

To deploy all metadata in one command, simple call the task called deploy_pre in a flow step. To be more specific call the same task, although add the option for the directory you want to deploy. For example:

example_flow:
  steps:
    1:
      task: deploy_pre
      options:
        path: unpackaged/pre/1_profiles

Note: The above would deploy only the metadata in the 1_profiles directory