FROM watsor.base

COPY . /opt/watsor

WORKDIR /opt/watsor

RUN python3 -m pip install -r requirements.txt && \
    rm -r /opt/watsor

USER watsor

WORKDIR /

CMD ["python3", "-m", "watsor.main", \
     "--log-path", "/var/log/watsor", \
     "--config", "/etc/watsor/config.yaml", \
     "--model-path", "/usr/share/watsor/model"]
