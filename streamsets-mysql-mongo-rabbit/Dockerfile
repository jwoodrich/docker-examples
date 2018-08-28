FROM streamsets/datacollector
RUN $SDC_DIST/bin/streamsets stagelibs -install=streamsets-datacollector-jdbc-lib,streamsets-datacollector-mongodb_3-lib,streamsets-datacollector-rabbitmq-lib
ENV MYSQL_DRIVER_VERSION 5.1.47
RUN mkdir -p $SDC_DIST/streamsets-libs-extras/streamsets-datacollector-jdbc-lib/lib && cd $SDC_DIST/streamsets-libs-extras/streamsets-datacollector-jdbc-lib/lib && curl -O http://central.maven.org/maven2/mysql/mysql-connector-java/$MYSQL_DRIVER_VERSION/mysql-connector-java-$MYSQL_DRIVER_VERSION.jar
