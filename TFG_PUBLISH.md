
## Upload package
Requirements: 
```
pip install twine
```
```
rm -rf dist
python setup.py sdist
twine upload dist/* --repository-url http://artifactory.tfgco.com/artifactory/api/pypi/pypi-local
```

## Add index
Add to the file `~/.pip/pip.conf`, using user `<USERNAME>` (User Profile: \<USERNAME>) and `<PASSWORD>` (API Key) found on https://artifactory.tfgco.com/artifactory/webapp/#/profile
```
[global]
extra-index-url = https://<USERNAME>:<PASSWORD>@artifactory.tfgco.com/artifactory/api/pypi/pypi/simple
trusted-host = artifactory.tfgco.com
```

## Download package
```
pip install tfg.jenkins-job-builder
```