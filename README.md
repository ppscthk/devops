```
docker run \
--rm \
-e JNLP_PROTOCOL_OPTS=-Dorg.jenkinsci.remoting.engine.JnlpProtocol3.disabled=false \
-v $(pwd)/jenkins_home:/var/jenkins_home \
-v /var/run/docker.sock:/var/run/docker.sock \
-v $(which docker):/usr/bin/docker \
-p 8080:8080 -p 50000:50000 \
-d --user root \
jenkinsci/blueocean
```
