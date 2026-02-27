- Builds, tests, and deployments are launched via YAML file instructions in GitLab. These instructions will run in stages based default stages in GitLab and can be also custom configured in the YAML file. The default stages are:
	- Build 
	- Test
	- Deploy

- Here is an example where the stages have been custom set:
  
  ![[GLCustomStages.png]]
- The jobs that run are listed below the stage instructions and are assigned to a stage as part of their configuration. 
- Jobs can also run in parallel. 

## Running Jobs in Parallel

- Jobs can be run in parallel simply by inputting them to the same stage. 
	- This can save on runtime of the pipeline and relieve complexity within the pipeline configuration. 

![[samestage.png]]

![[pipelinepara.png]]

## Links:

[[GitLab CI CD]]

2025111758