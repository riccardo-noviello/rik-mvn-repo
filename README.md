# rik-mvn-repo
This is a github repository for some of my projects. You can download a snapshot of my work as a maven dependency. Here is how:


1. add target
 ```
    <distributionManagement>
    <repository>
        <id>repo</id>
        <url>https://github.com/rik86/rik-mvn-repo/raw/master/releases</url>
    </repository>
    <snapshotRepository>
        <id>snapshot-repo</id>
        <url>https://github.com/rik86/rik-mvn-repo/raw/master/snapshots</url>
    </snapshotRepository>
</distributionManagement>
 ```

2. deploy
 ```mvn -DaltDeploymentRepository=snapshot-repo::default::file:../../rik-mvn-repo/snapshots clean deploy ```

3. push jar to rik-mvn-repo

4. Use dependency
 ```
<repositories>
    <repository>
        <id>rik-snapshots</id>
        <url>https://github.com/rik86/rik-mvn-repo/raw/master/snapshots</url>
    </repository>
</repositories>

 ```
