# choose system ---------------------------------------------------
FROM  centos 
#FROM chanchal/rhel72
#FROM  darksolar/rhel6.6-gcc4.9	

#0st layer
RUN yum -y update; yum clean all
RUN yum -y install epel-release; yum clean all
RUN yum install -y gcc;  yum clean all
#1st layer
# ---------------------------------------------------
ADD ecloud.tar.gz /
# 3d layer -----------------------------------------
COPY rules /opt/ecloud/rules
# 4d layer -----------------------------------------
RUN /opt/ecloud/rules/install
#----------------------------------------------------
# supervisor script --------------------------------
CMD ["/opt/ecloud/rules/auto"]
# ---------------------------------------------------
