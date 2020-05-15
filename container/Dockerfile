FROM registry.access.redhat.com/rhel7/rhel-tools
RUN yum update -y && yum install -y openssh-server openssh-clients jq origin-clients openscap-scanner scap-security-guide && yum clean all

RUN echo "%wheel  ALL=(ALL)       NOPASSWD: ALL" >> /etc/sudoers

COPY launch.sh /bin/
RUN chmod +x /bin/launch.sh

CMD /bin/launch.sh
