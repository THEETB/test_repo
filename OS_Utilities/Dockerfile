ARG RELEASE_TAG
FROM bala001/centos:${RELEASE_TAG}

RUN echo "installing centos rpms..." \
    && yum clean all \
    && echo "local repository file for centos8 rpms.." \
    && yum install -y epel-release \
    && yum groupinstall -y "Development Tools" \
    && yum install -y  shadow-utils \
    && yum install -y libpng-devel  librsvg2-devel libpng-devel libjpeg-turbo-devel wget \
    && echo "clearing up RPMS local Repository" \
    && rm -rf /etc/yum.repos.d/Centos77-Local.repo \
    && yum clean all


ENV LD_LIBRARY_PATH=/pkpd/gdal-2.4.2/lib:usr/lib/oracle/19.3/client64/lib:/pkpd/gdal-2.4.2/lib:/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.222.b10-0.el7_6.x86_64/jre/lib/amd64/server
ENV OCI_LIB=/usr/lib/oracle/19.3/client64/lib/
ENV TNS_ADMIN=/opt/oracle/network/admin
ENV PATH=/opt/Qt5.14.2/5.14.2/gcc_64/bin/:/pkpd/bin:/pkpd/R-4.0.3/bin:/pkpd/perl-5.30.0/bin:/pkpd/gdal-2.4.2/bin:/usr/local/texlive/2019/bin/x86_64-linux:/usr/lib/oracle/19.3/client64/bin:/pkpd/gdal-2.4.2/bin:/usr/share/centrifydc/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/pkpd/Lixoft/MonolixSuite2020R1:/pkpd/Lixoft/MonolixSuite2020R1/bin
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.222.b10-0.el7_6.x86_64/jre
ENV GDAL_DATA=/pkpd/gdal-2.4.2/share/gdal
ENV OCI_INC=/usr/include/oracle/19.3/client64
ENV RSTUDIO_CHROMIUM_ARGUMENTS=--disable-gpu
ENV R_JAVA_LD_LIBRARY_PATH=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.222.b10-0.el7_6.x86_64/jre/lib/amd64/server
ENV NOAWT=1
