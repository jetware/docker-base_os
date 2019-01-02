FROM centos:7
LABEL org.jetware.base_os="centos" org.jetware.base_os.version="7"
RUN yum install -y sudo wget libcap
RUN useradd --system -u 999 -d "/jet" -s "/jet/login" jet
