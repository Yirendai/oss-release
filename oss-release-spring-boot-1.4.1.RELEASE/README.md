
# oss-release-spring-boot-1.4.1.RELEASE

使用spring-boot-1.4.1.RELEASE的用户需要使用oss-release-spring-boot-1.4.1.RELEASE引入oss-common-dependencies-spring-boot-1.4.1.RELEASE和针对spring-boot-1.4.1测试并构建的oss-lib.

## 使用方法

你的项目可以使用oss-release作为parent, 这样间接地以oss-build为ancestor.

    <parent>
        <groupId>com.yirendai.oss</groupId>
        <artifactId>oss-release-spring-boot-1.4.1.RELEASE</artifactId>
        <version>${oss-release.version}</version>
    </parent>

或者在dependencyManagement中import它.

    <!-- 以oss-build为parent是可选的 -->
    <parent>
        <groupId>com.yirendai.oss</groupId>
        <artifactId>oss-build</artifactId>
        <version>${oss-build.version}</version>
    </parent>
    <dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>com.yirendai.oss</groupId>
                <artifactId>oss-release-spring-boot-1.4.1.RELEASE</artifactId>
                <version>${oss-release.version}</version>
                <type>pom</type>
                <scope>import</scope>
            </dependency>
        </dependencies>
    </dependencyManagement>
