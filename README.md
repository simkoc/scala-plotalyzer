# Plotalyzer

This is the sibling program to the [appanalyzer](https://github.com/simkoc/scala-appanalyzer). 
The plotalyze will assist with evaluating the collected information during app analysis via a plugin system.
You can use and install already known plugins using the plugin manager or you can write your own.
Each plugin provides its own unique capability of analyzing the collected data and outputting them in a human readable form, usually json.




## Writing your own plugin

To write your own plugin you need to depend on this repository. It is publicly available

```
ThisBuild / resolvers ++= Seq(
  "Sonatype OSS Snapshots" at "https://s01.oss.sonatype.org/content/repositories/public",
)
libraryDependencies ++= Seq("de.halcony" %% "plotalyzer" %% "1.0.0") 
```

you then need to implement the `AnalysisPlugin` interface. Move the packaged jar of your project into the plugin folder
to make the plugin locally available.