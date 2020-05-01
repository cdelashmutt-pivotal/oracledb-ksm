KSM Artifacts to provide a Single Instance Oracle XE databse as a self service via Helm.

# To Use
* Build and push an Oracle XE container image by following the instructions at https://github.com/oracle/docker-images/blob/master/OracleDatabase/SingleInstance/README.md
* Push the resulting image to the private image repository your KSM installation is configured to use.
* Clone the repo at https://github.com/cdelashmutt-pivotal/oracledb-on-k8s, and the `cd` into the `oracledb` subdirectory of that repo.
* Execute `helm package .`.
* Copy the resulting `oracledb-*.tgz` file to the directory containing this README.md file.
* Use the KSM CLI to create the service offering: https://docs.pivotal.io/ksm/0-5/using.html#add
* Enable access to the new service offering using the CF CLI: `cf enable-service-access oracledb` 