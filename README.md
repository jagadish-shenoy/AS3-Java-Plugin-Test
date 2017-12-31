# AS3-Java-Plugin-Test
Gradle java plugin is not working correctly in android Studio 3.0 .

<b>Background:</b> 

I have an android project with a few Java Modules. One of the java modules has a jar dependency. Since this jar is legacy and not available via Maven repository, the jar file is in libs directory of the module and jar was included in the class path using  

<code>compile fileTree(dir: 'libs', include: ['*.jar'])</code> - everything worked fine in Android studio 2.0  

Issue:

But with Android studio 3.0, ClassNotFoundException is thrown at runtime for the classes in the jar, detailed analysis releved that classes from the jar file not included at all in the final output!.

build.gradle for the module with jar dependency is as below:
<code>
apply plugin: 'java'

dependencies {
   compile fileTree(dir: 'libs', include: ['*.jar'])
   //compile project(':SampleJar') //-- This works!
}

sourceCompatibility = "1.7"
targetCompatibility = "1.7"

</code>

I have verified this gradle configuration from IntelliJ IDEA, things just work fine.

Structure of this Sample code:
