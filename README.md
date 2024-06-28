# Local setup

using node version 16.14.2
```bash
npm install
```

# Build and run

You can build and run local development server like this
```bash
yarn dev:ssr
```

# Test

`yarn e2e` or `yarn e2e --watch`, latest recommended for development

# Docs

[Design](https://app.zeplin.io/project/5d3aef8cc04b656bbaf691cd/dashboard)

[API](https://gold-desert-2099.postman.co/collections/3483235-dce47c30-9656-4e53-b1cc-5f89ccd2e3b3?version=latest&workspace=f2b4c53f-2727-46fa-8513-e149f5cc0dcc#0daa9c96-fff7-4161-9e03-a777bdcf21d2)

# Setup digitalocean ubuntu and apache

[Guide](https://www.cloudbooklet.com/setup-node-js-with-apache-proxy-on-ubuntu-18-04-for-production/)

Create folder structure

```bash
mkdir /root/oigetit-web
mkdir /root/oigetit-web/dist
```

# Deploy

Build the project
```bash
yarn build:ssr
```

Copy to remote server
```bash
scp -i <your_ssh_key> -r <path_to_dist_folder> root@<remote_server>:/root/oigetit-web/
```

Run the server
```bash
pm2 start dist/apps/oigetit-web/server/main.js
```

# Builds and Branches

Please create your own branch to work on changes/bug-fixs and commit to this branch. When you done make a pull request to Master.
