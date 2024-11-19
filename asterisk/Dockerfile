FROM alpine:latest

RUN apk add asterisk

ADD ari.conf /etc/asterisk/
ADD extensions.conf /etc/asterisk/
ADD http.conf /etc/asterisk/
ADD modules.conf /etc/asterisk/
ADD pjsip.conf /etc/asterisk/

CMD asterisk -f
