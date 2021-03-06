swagger: "2.0"
x-collection-name: AWS Elastic Beanstalk
x-complete: 1
info:
  title: AWS Elastic Beanstalk API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AbortEnvironmentUpdate:
    get:
      summary: Abort Environment Update
      description: |-
        Cancels in-progress environment configuration update or application version
              deployment.
      operationId: abortEnvironmentUpdate
      x-api-path-slug: actionabortenvironmentupdate-get
      parameters:
      - in: query
        name: EnvironmentId
        description: This specifies the ID of the environment with the in-progress
          update that you want to      cancel
        type: string
      - in: query
        name: EnvironmentName
        description: This specifies the name of the environment with the in-progress
          update that you want to      cancel
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=ApplyEnvironmentManagedAction:
    get:
      summary: Apply Environment Managed Action
      description: Applies a scheduled managed action immediately.
      operationId: applyEnvironmentManagedAction
      x-api-path-slug: actionapplyenvironmentmanagedaction-get
      parameters:
      - in: query
        name: ActionId
        description: The action ID of the scheduled managed action to execute
        type: string
      - in: query
        name: EnvironmentId
        description: The environment ID of the target environment
        type: string
      - in: query
        name: EnvironmentName
        description: The name of the target environment
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=ComposeEnvironments:
    get:
      summary: Compose Environments
      description: |-
        Create or update a group of environments that each run a separate component of a single
              application.
      operationId: composeEnvironments
      x-api-path-slug: actioncomposeenvironments-get
      parameters:
      - in: query
        name: ApplicationName
        description: The name of the application to which the specified source bundles
          belong
        type: string
      - in: query
        name: GroupName
        description: The name of the group to which the target environments belong
        type: string
      - in: query
        name: VersionLabels.member.N
        description: A list of version labels, specifying one or more application
          source bundles that belong      to the target application
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=CreateEnvironment:
    get:
      summary: Create Environment
      description: |-
        Launches an environment for the specified application using the specified
              configuration.
      operationId: createEnvironment
      x-api-path-slug: actioncreateenvironment-get
      parameters:
      - in: query
        name: ApplicationName
        description: The name of the application that contains the version to be deployed
        type: string
      - in: query
        name: CNAMEPrefix
        description: If specified, the environment attempts to use this value as the
          prefix for the CNAME
        type: string
      - in: query
        name: Description
        description: Describes this environment
        type: string
      - in: query
        name: EnvironmentName
        description: A unique name for the deployment environment
        type: string
      - in: query
        name: GroupName
        description: The name of the group to which the target environment belongs
        type: string
      - in: query
        name: OptionSettings.member.N
        description: If specified, AWS Elastic Beanstalk sets the specified configuration
          options to the      requested value in the configuration set for the new
          environment
        type: string
      - in: query
        name: OptionsToRemove.member.N
        description: A list of custom user-defined configuration options to remove
          from the configuration      set for this new environment
        type: string
      - in: query
        name: SolutionStackName
        description: This is an alternative to specifying a template name
        type: string
      - in: query
        name: Tags.member.N
        description: This specifies the tags applied to resources in the environment
        type: string
      - in: query
        name: TemplateName
        description: The name of the configuration template to use in deployment
        type: string
      - in: query
        name: Tier
        description: This specifies the tier to use for creating this environment
        type: string
      - in: query
        name: VersionLabel
        description: The name of the application version to deploy
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=DeleteEnvironmentConfiguration:
    get:
      summary: Delete Environment Configuration
      description: Deletes the draft configuration associated with the running environment.
      operationId: deleteEnvironmentConfiguration
      x-api-path-slug: actiondeleteenvironmentconfiguration-get
      parameters:
      - in: query
        name: ApplicationName
        description: The name of the application the environment is associated with
        type: string
      - in: query
        name: EnvironmentName
        description: The name of the environment to delete the draft configuration
          from
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=DescribeEnvironmentHealth:
    get:
      summary: Describe Environment Health
      description: Returns information about the overall health of the specified environment.
      operationId: describeEnvironmentHealth
      x-api-path-slug: actiondescribeenvironmenthealth-get
      parameters:
      - in: query
        name: AttributeNames.member.N
        description: Specify the response elements to return
        type: string
      - in: query
        name: EnvironmentId
        description: Specify the environment by ID
        type: string
      - in: query
        name: EnvironmentName
        description: Specify the environment by name
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=DescribeEnvironmentManagedActionHistory:
    get:
      summary: Describe Environment Managed Action History
      description: Lists an environment's completed and failed managed actions.
      operationId: describeEnvironmentManagedActionHistory
      x-api-path-slug: actiondescribeenvironmentmanagedactionhistory-get
      parameters:
      - in: query
        name: EnvironmentId
        description: The environment ID of the target environment
        type: string
      - in: query
        name: EnvironmentName
        description: The name of the target environment
        type: string
      - in: query
        name: MaxItems
        description: The maximum number of items to return for a single request
        type: string
      - in: query
        name: NextToken
        description: The pagination token returned by a previous request
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=DescribeEnvironmentManagedActions:
    get:
      summary: Describe Environment Managed Actions
      description: Lists an environment's upcoming and in-progress managed actions.
      operationId: describeEnvironmentManagedActions
      x-api-path-slug: actiondescribeenvironmentmanagedactions-get
      parameters:
      - in: query
        name: EnvironmentId
        description: The environment ID of the target environment
        type: string
      - in: query
        name: EnvironmentName
        description: The name of the target environment
        type: string
      - in: query
        name: Status
        description: To show only actions with a particular status, specify a status
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=DescribeEnvironmentResources:
    get:
      summary: Describe Environment Resources
      description: Returns AWS resources for this environment.
      operationId: describeEnvironmentResources
      x-api-path-slug: actiondescribeenvironmentresources-get
      parameters:
      - in: query
        name: EnvironmentId
        description: The ID of the environment to retrieve AWS resource usage data
        type: string
      - in: query
        name: EnvironmentName
        description: The name of the environment to retrieve AWS resource usage data
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=DescribeEnvironments:
    get:
      summary: Describe Environments
      description: Returns descriptions for existing environments.
      operationId: describeEnvironments
      x-api-path-slug: actiondescribeenvironments-get
      parameters:
      - in: query
        name: ApplicationName
        description: If specified, AWS Elastic Beanstalk restricts the returned descriptions
          to include only      those that are associated with this application
        type: string
      - in: query
        name: EnvironmentIds.member.N
        description: If specified, AWS Elastic Beanstalk restricts the returned descriptions
          to include only      those that have the specified IDs
        type: string
      - in: query
        name: EnvironmentNames.member.N
        description: If specified, AWS Elastic Beanstalk restricts the returned descriptions
          to include only      those that have the specified names
        type: string
      - in: query
        name: IncludedDeletedBackTo
        description: If specified when IncludeDeleted is set to true, then      environments
          deleted after this date are displayed
        type: string
      - in: query
        name: IncludeDeleted
        description: 'Indicates whether to include deleted environments:'
        type: string
      - in: query
        name: VersionLabel
        description: If specified, AWS Elastic Beanstalk restricts the returned descriptions
          to include only      those that are associated with this application version
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=RebuildEnvironment:
    get:
      summary: Rebuild Environment
      description: |-
        Deletes and recreates all of the AWS resources (for example: the Auto Scaling group,
              load balancer, etc.
      operationId: rebuildEnvironment
      x-api-path-slug: actionrebuildenvironment-get
      parameters:
      - in: query
        name: EnvironmentId
        description: The ID of the environment to rebuild
        type: string
      - in: query
        name: EnvironmentName
        description: The name of the environment to rebuild
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=RequestEnvironmentInfo:
    get:
      summary: Request Environment Info
      description: |-
        Initiates a request to compile the specified type of information of the deployed
              environment.
      operationId: requestEnvironmentInfo
      x-api-path-slug: actionrequestenvironmentinfo-get
      parameters:
      - in: query
        name: EnvironmentId
        description: The ID of the environment of the requested data
        type: string
      - in: query
        name: EnvironmentName
        description: The name of the environment of the requested data
        type: string
      - in: query
        name: InfoType
        description: The type of information to request
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=RetrieveEnvironmentInfo:
    get:
      summary: Retrieve Environment Info
      description: Retrieves the compiled information from a.
      operationId: retrieveEnvironmentInfo
      x-api-path-slug: actionretrieveenvironmentinfo-get
      parameters:
      - in: query
        name: EnvironmentId
        description: The ID of the datas environment
        type: string
      - in: query
        name: EnvironmentName
        description: The name of the datas environment
        type: string
      - in: query
        name: InfoType
        description: The type of information to retrieve
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=SwapEnvironmentCNAMEs:
    get:
      summary: Swap Environment C N A M Es
      description: Swaps the CNAMEs of two environments.
      operationId: swapEnvironmentCNAMEs
      x-api-path-slug: actionswapenvironmentcnames-get
      parameters:
      - in: query
        name: DestinationEnvironmentId
        description: The ID of the destination environment
        type: string
      - in: query
        name: DestinationEnvironmentName
        description: The name of the destination environment
        type: string
      - in: query
        name: SourceEnvironmentId
        description: The ID of the source environment
        type: string
      - in: query
        name: SourceEnvironmentName
        description: The name of the source environment
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=TerminateEnvironment:
    get:
      summary: Terminate Environment
      description: Terminates the specified environment.
      operationId: terminateEnvironment
      x-api-path-slug: actionterminateenvironment-get
      parameters:
      - in: query
        name: EnvironmentId
        description: The ID of the environment to terminate
        type: string
      - in: query
        name: EnvironmentName
        description: The name of the environment to terminate
        type: string
      - in: query
        name: ForceTerminate
        description: Terminates the target environment even if another environment
          in the same group is      dependent on it
        type: string
      - in: query
        name: TerminateResources
        description: 'Indicates whether the associated AWS resources should shut down
          when the environment is      terminated:'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments
  /?Action=UpdateEnvironment:
    get:
      summary: Update Environment
      description: |-
        Updates the environment description, deploys a new application version, updates the
              configuration settings to an entirely new configuration template, or updates select
              configuration option values in the running environment.
      operationId: updateEnvironment
      x-api-path-slug: actionupdateenvironment-get
      parameters:
      - in: query
        name: ApplicationName
        description: The name of the application with which the environment is associated
        type: string
      - in: query
        name: Description
        description: If this parameter is specified, AWS Elastic Beanstalk updates
          the description of this      environment
        type: string
      - in: query
        name: EnvironmentId
        description: The ID of the environment to update
        type: string
      - in: query
        name: EnvironmentName
        description: The name of the environment to update
        type: string
      - in: query
        name: GroupName
        description: The name of the group to which the target environment belongs
        type: string
      - in: query
        name: OptionSettings.member.N
        description: If specified, AWS Elastic Beanstalk updates the configuration
          set associated with the      running environment and sets the specified
          configuration options to the requested      value
        type: string
      - in: query
        name: OptionsToRemove.member.N
        description: A list of custom user-defined configuration options to remove
          from the configuration      set for this environment
        type: string
      - in: query
        name: SolutionStackName
        description: This specifies the platform version that the environment will
          run after the environment      is updated
        type: string
      - in: query
        name: TemplateName
        description: If this parameter is specified, AWS Elastic Beanstalk deploys
          this configuration      template to the environment
        type: string
      - in: query
        name: Tier
        description: This specifies the tier to use to update the environment
        type: string
      - in: query
        name: VersionLabel
        description: If this parameter is specified, AWS Elastic Beanstalk deploys
          the named application      version to the environment
        type: string
      responses:
        200:
          description: OK
      tags:
      - Environments