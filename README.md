# OpenShift Template for Bitrix + MySQL (Persistent storage)

This is a template that you can use to create a OpenShift cluster for [Bitrix CMS](https://www.1c-bitrix.ru/) with MySQL Database

## What has been done for you

This template will create:

1. Build configuration based on official [php:5.6-apache](https://hub.docker.com/_/php/) image
2. Deployment configuration for Application and Database servers
3. Router with default route to application server

## How to use

`oc process bitrix_template.json -p SOURCE_REPOSITORY_URL='<your git>' -p BITRIX_LICENSE_KEY='<license>' -p BITRIX_URL='http://<url-to-bitrix-archive>' | oc create -f -`

### Parameters:
- `SOURCE_REPOSITORY_URL` - Git repository for your project
- `BITRIX_LICENSE_KEY` - License number for Bitrix
- `BITRIX_URL` - URL to tar.gz file which contains core file of Bitrix

## TODO

- `CONTEXT_DIR` parametr is not working
- Upload directory is on ephemeral storage
- ...more

## License

This code is dedicated to the public domain to the maximum extent permitted by applicable law, pursuant to [CC0](http://creativecommons.org/publicdomain/zero/1.0/).