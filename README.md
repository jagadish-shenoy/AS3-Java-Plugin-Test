# AS3-Java-Plugin-Test
Gradle java plugin not working correctly in android Studio 3.0  I have an android project with a few Java Modules. One of the java modules has a jar dependency. As usual the jar file is in libs directory of the module and jar was included in the class path using   compile fileTree(dir: 'libs', include: ['*.jar']) - everything worked fine in Android studio 2.0  But with Android studio 3.0, I am getting ClassNotFoundException at runtime for classes from the jar file.