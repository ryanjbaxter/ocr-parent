# ocr-parent
Parent POM for OCR apps

# Deploying

`./mvnw deploy -s settings.xml`

You need to set the following environment variables 

`$ export SONATYPE_USER=username`
`$ export SONATYPE_PASSWORD=password`

# Concourse CI

To use the Concourse pipeline run

`$ fly -t local set-pipeline --pipeline ocr-parent --config ci/pipelines/ocr-parent.yml --var "SONATYPE_USER=username" --var "SONATYPE_PASSWORD=password"`
