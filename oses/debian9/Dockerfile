FROM debian:9-slim
RUN apt-get update && \
		apt-get install -y netbase sudo wget libcap2-bin && \
		find /var/lib/apt/lists -type f -size +0 -delete

RUN useradd --system -u 999 -d "/jet" -s "/jet/login" jet
