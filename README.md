# jenkins_docker_pipeline_tutorial1
Code base for tutorial: Dockerizing Jenkins 2 setup and using it along with Sonarqube to create modern declarative build pipeline. 

Choose the suggested plugins option and Jenkins will start the installation of plugins. Once this is done, we need to capture the plugins installed and then automate them in Docker.

Open http://localhost:8080/script and paste this Groovy script and run it:

```
Jenkins.instance.pluginManager.plugins.each{
 plugin ->
   println ("${plugin.getShortName()}:${plugin.getVersion()}")
}

```

Now, copy plugins that are displayed in the list- that is, all text from the top, up to the “Result:” section and create a file plugins.txt and paste the copied text there.
