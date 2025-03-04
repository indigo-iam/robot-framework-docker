FROM almalinux:9

ARG USERNAME=test
ARG USER_UID=1000
ARG USER_GID=${USER_UID}

COPY /scripts/*.sh /tmp/scripts/

RUN   dnf install -y epel-release && \
      curl -L https://repo.data.kit.edu//data-kit-edu-almalinux9.repo -o /etc/yum.repos.d/data-kit-edu-almalinux9.repo && \
      dnf -y update && \
      dnf -y install git which sudo jq \
        voms-clients-cpp voms-clients-java python3-gfal2-util gfal2-all python3-gfal2 davix oidc-agent \
        python3-pip python3-devel python3-setuptools && \
      dnf module install -y nodejs:18 && \
      npm install -g jwt-cli && \
      rm -rf /var/cache/dnf && \
      bash /tmp/scripts/provide-user.sh ${USERNAME} ${USER_UID} ${USER_GID} && \
      mkdir /home/${USERNAME}/.config /home/${USERNAME}/.globus && \
      chown -R ${USERNAME}:${USERNAME} /home/${USERNAME} && \
      bash /tmp/scripts/provide-robotframework.sh && \
      rm -rf /tmp/scripts

USER ${USERNAME}
WORKDIR /home/${USERNAME}
