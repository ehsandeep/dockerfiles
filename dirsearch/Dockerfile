# Basic usage:
# docker run -it --rm wfnintr/dirsearch -u target -e php,html,png,js,jpg
FROM python:3-alpine
LABEL source="<github.com/maurosoria/dirsearch>"
LABEL maintainer="wfnintr@null.net"
WORKDIR /root
RUN apk add --no-cache --virtual .depends git 
RUN git clone https://github.com/maurosoria/dirsearch.git
RUN apk del .depends
WORKDIR /root/dirsearch
ENTRYPOINT ["./dirsearch.py"]
CMD ["--help"]
