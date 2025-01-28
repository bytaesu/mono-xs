![mono-xs-img](https://github.com/user-attachments/assets/d488eb4e-33b4-4a57-b94e-733cbe742535)

# Introduction

`mono-xs` offers a monorepo structure that leverages [Turborepo](https://turbo.build/repo/docs) to efficiently manage [Next.js](https://nextjs.org) and [Nestjs](https://nestjs.com) applications.

This is a primitive template generated using the Turborepo CLI and NestJS CLI, so feel free to modify it to fit your specific needs and start developing. You don’t have to use everything in the template.

I've recently been enjoying deploying the backend to the [Fly.io](https://fly.io) platform, so Dockerfiles and related configurations are included.

While this setup enables deployment to multiple platforms, if you, like me, also favor Fly.io, you'll find that there's virtually no configuration needed from development to deployment.

### Required Knowledge:

- Monorepo structure (in this case, using Turborepo)
- Docker (if you intend to use Fly.io)
- Nestjs framework
- Next.js framework

<br/>

# Deployment Guide

In this section, the process of deploying to the [Fly.io](https://fly.io) platform is briefly explained.

### 1. Create Apps on Fly

```sh
fly apps create
```
### 2. Configure the fly.toml

Refer to [Fly.io Docs](https://fly.io/docs/reference/configuration)

The necessary details have been commented in each fly.toml file.

### 3. Deploy

```sh
# Deploy a Single App

fly deploy --config fly.your-fly-app-name.toml

```

```sh
# Deploy All at Once
# You need to specify the respective fly.toml file names in the fly.deploy.sh file.

chmod +x fly.deploy.sh

./fly.deploy.sh
```

<br/>

# In closing

You can attach your desired database stack and use it with this. (I use PostgreSQL)

I prefer to avoid repetitive tasks and enjoy increasing productivity. I believe this repository will be very helpful for specific workflows.

**Develop your ideas fast, ship them even faster🚀**

[> Reference I used](https://github.com/HelixHEX/fly-monorepo-demo)
