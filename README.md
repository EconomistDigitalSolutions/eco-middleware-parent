# ECO Middleware Parent
This repository contains a maven parent project for use by all CASE ESB (Mule) middleware applications.
Indeed it can be used by all Java Maven projects within the enterprise, however the group Id has been chosen to not clash
with other application structures within the organisation.

## CI/CD
This project (and subsequent child projects) are setup in a way to enable Continuous Delivery of artifacts into the
deployment spaces of the organisation. This is achieved without the use of the Maven Release plugin as this is cumbersome.

For more information as to why the Maven Release plugin is not used, please see the References section of this ReadMe.

CI is provided in Circle CI. As a result the code within the repository contains its own settings xml (.circleci.settings.xml)
to be used by Circle CI. The files are sanitised to ensure that no passwords are stored within them.

## References
- [Maven Releases on Steroids: Adios Release Plugin!](https://axelfontaine.com/blog/maven-releases-steroids.html)