FROM ubuntu:18.04
LABEL org.jetware.base_os="ubuntu" org.jetware.base_os.version="18.04"
RUN \
  echo "tzdata tzdata/Areas select Etc" | debconf-set-selections; \
  echo "tzdata tzdata/Zones/Etc select Universal" | debconf-set-selections; \
  apt-get update && \
    DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true \
      apt-get install -y tzdata netbase sudo wget libcap2-bin && \
	  find /var/lib/apt/lists -type f -size +0 -delete

RUN useradd --system -u 999 -d "/jet" -s "/jet/login" jet
