FROM almalinux:9
RUN dnf install telnet net-tools iputils -y
RUN useradd roboshop
USER roboshop
CMD ["sleep", "100000"]


# docker push with syam/debug:v1