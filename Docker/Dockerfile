FROM alpine:3

COPY entrypoint.sh /entrypoint.sh
COPY requirements.txt /requirements.txt

RUN apk add --no-cache openssh python3 python3-dev py3-pip py3-cryptography git build-base
RUN pip3 install --no-cache -r /requirements.txt

COPY ansible.cfg /etc/ansible/ansible.cfg

ENTRYPOINT ["/entrypoint.sh"]
