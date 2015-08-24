# rik-mvn-repo

1. add target

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

2. deploy
mvn -DaltDeploymentRepository=snapshot-repo::default::file:../../rik86-mvn-repo/snapshots clean deploy

3. push jar to rik-mvn-repo

4. Use dependency

<repositories>
    <repository>
        <id>rik-snapshots</id>
        <url>https://github.com/rik86/rik-mvn-repo/raw/master/snapshots</url>
    </repository>
</repositories>

