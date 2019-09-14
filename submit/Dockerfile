FROM bde2020/hadoop-base

MAINTAINER Ivan Ermilov <ivan.s.ermilov@gmail.com>

COPY AvroGenericStationTempYear.jar /opt/hadoop/applications/AvroGenericStationTempYear.jar
COPY ./config/weather.avsc /opt/hadoop/applications/weather.avsc
# COPY NCDC-Weather_small.txt /opt/hadoop/applications/NCDC-Weather_small.txt

ENV JAR_FILEPATH="/opt/hadoop/applications/AvroGenericStationTempYear.jar"
ENV CLASS_TO_RUN=""
ENV PARAMS="/input /output /opt/hadoop/applications/weather.avsc"

ADD run.sh /run.sh
RUN chmod a+x /run.sh

CMD ["/run.sh"]
