<!-- markdownlint-disable MD030 -->

<img width="100%" src="https://github.com/Aethon LabsAI/Aethon Labs/blob/main/images/Aethon Labs.png?raw=true"></a>

# Aethon Labs - Build LLM Apps Easily

[![Release Notes](https://img.shields.io/github/release/Aethon LabsAI/Aethon Labs)](https://github.com/Aethon LabsAI/Aethon Labs/releases)
[![Discord](https://img.shields.io/discord/1087698854775881778?label=Discord&logo=discord)](https://discord.gg/jbaHfsRVBW)
[![Twitter Follow](https://img.shields.io/twitter/follow/Aethon LabsAI?style=social)](https://twitter.com/Aethon LabsAI)
[![GitHub star chart](https://img.shields.io/github/stars/Aethon LabsAI/Aethon Labs?style=social)](https://star-history.com/#Aethon LabsAI/Aethon Labs)
[![GitHub fork](https://img.shields.io/github/forks/Aethon LabsAI/Aethon Labs?style=social)](https://github.com/Aethon LabsAI/Aethon Labs/fork)

English | [繁體中文](./i18n/README-TW.md) | [简体中文](./i18n/README-ZH.md) | [日本語](./i18n/README-JA.md) | [한국어](./i18n/README-KR.md)

<h3>Drag & drop UI to build your customized LLM flow</h3>
<a href="https://github.com/Aethon LabsAI/Aethon Labs">
<img width="100%" src="https://github.com/Aethon LabsAI/Aethon Labs/blob/main/images/Aethon Labs.gif?raw=true"></a>

## ⚡Quick Start

Download and Install [NodeJS](https://nodejs.org/en/download) >= 18.15.0

1. Install Aethon Labs
    ```bash
    npm install -g Aethon Labs
    ```
2. Start Aethon Labs

    ```bash
    npx Aethon Labs start
    ```

    With username & password

    ```bash
    npx Aethon Labs start --Aethon Labs_USERNAME=user --Aethon Labs_PASSWORD=1234
    ```

3. Open [http://localhost:3000](http://localhost:3000)

## 🐳 Docker

### Docker Compose

1. Clone the Aethon Labs project
2. Go to `docker` folder at the root of the project
3. Copy `.env.example` file, paste it into the same location, and rename to `.env` file
4. `docker compose up -d`
5. Open [http://localhost:3000](http://localhost:3000)
6. You can bring the containers down by `docker compose stop`

### Docker Image

1. Build the image locally:
    ```bash
    docker build --no-cache -t Aethon Labs .
    ```
2. Run image:

    ```bash
    docker run -d --name Aethon Labs -p 3000:3000 Aethon Labs
    ```

3. Stop image:
    ```bash
    docker stop Aethon Labs
    ```

## 👨‍💻 Developers

Aethon Labs has 3 different modules in a single mono repository.

-   `server`: Node backend to serve API logics
-   `ui`: React frontend
-   `components`: Third-party nodes integrations
-   `api-documentation`: Auto-generated swagger-ui API docs from express

### Prerequisite

-   Install [PNPM](https://pnpm.io/installation)
    ```bash
    npm i -g pnpm
    ```

### Setup

1.  Clone the repository

    ```bash
    git clone https://github.com/Aethon LabsAI/Aethon Labs.git
    ```

2.  Go into repository folder

    ```bash
    cd Aethon Labs
    ```

3.  Install all dependencies of all modules:

    ```bash
    pnpm install
    ```

4.  Build all the code:

    ```bash
    pnpm build
    ```

    <details>
    <summary>Exit code 134 (JavaScript heap out of memory)</summary>  
      If you get this error when running the above `build` script, try increasing the Node.js heap size and run the script again:

        export NODE_OPTIONS="--max-old-space-size=4096"
        pnpm build

    </details>

5.  Start the app:

    ```bash
    pnpm start
    ```

    You can now access the app on [http://localhost:3000](http://localhost:3000)

6.  For development build:

    -   Create `.env` file and specify the `VITE_PORT` (refer to `.env.example`) in `packages/ui`
    -   Create `.env` file and specify the `PORT` (refer to `.env.example`) in `packages/server`
    -   Run

        ```bash
        pnpm dev
        ```

    Any code changes will reload the app automatically on [http://localhost:8080](http://localhost:8080)

## 🔒 Authentication

To enable app level authentication, add `Aethon Labs_USERNAME` and `Aethon Labs_PASSWORD` to the `.env` file in `packages/server`:

```
Aethon Labs_USERNAME=user
Aethon Labs_PASSWORD=1234
```

## 🌱 Env Variables

Aethon Labs support different environment variables to configure your instance. You can specify the following variables in the `.env` file inside `packages/server` folder. Read [more](https://github.com/Aethon LabsAI/Aethon Labs/blob/main/CONTRIBUTING.md#-env-variables)

## 📖 Documentation

[Aethon Labs Docs](https://docs.Aethon Labsai.com/)

## 🌐 Self Host

Deploy Aethon Labs self-hosted in your existing infrastructure, we support various [deployments](https://docs.Aethon Labsai.com/configuration/deployment)

-   [AWS](https://docs.Aethon Labsai.com/configuration/deployment/aws)
-   [Azure](https://docs.Aethon Labsai.com/configuration/deployment/azure)
-   [Digital Ocean](https://docs.Aethon Labsai.com/configuration/deployment/digital-ocean)
-   [GCP](https://docs.Aethon Labsai.com/configuration/deployment/gcp)
-   [Alibaba Cloud](https://computenest.console.aliyun.com/service/instance/create/default?type=user&ServiceName=Aethon Labs社区版)
-   <details>
      <summary>Others</summary>

    -   [Railway](https://docs.Aethon Labsai.com/configuration/deployment/railway)

        [![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/template/pn4G8S?referralCode=WVNPD9)

    -   [Render](https://docs.Aethon Labsai.com/configuration/deployment/render)

        [![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://docs.Aethon Labsai.com/configuration/deployment/render)

    -   [HuggingFace Spaces](https://docs.Aethon Labsai.com/deployment/hugging-face)

        <a href="https://huggingface.co/spaces/Aethon LabsAI/Aethon Labs"><img src="https://huggingface.co/datasets/huggingface/badges/raw/main/open-in-hf-spaces-sm.svg" alt="HuggingFace Spaces"></a>

    -   [Elestio](https://elest.io/open-source/Aethon Labsai)

        [![Deploy on Elestio](https://elest.io/images/logos/deploy-to-elestio-btn.png)](https://elest.io/open-source/Aethon Labsai)

    -   [Sealos](https://cloud.sealos.io/?openapp=system-template%3FtemplateName%3DAethon Labs)

        [![](https://raw.githubusercontent.com/labring-actions/templates/main/Deploy-on-Sealos.svg)](https://cloud.sealos.io/?openapp=system-template%3FtemplateName%3DAethon Labs)

    -   [RepoCloud](https://repocloud.io/details/?app_id=29)

        [![Deploy on RepoCloud](https://d16t0pc4846x52.cloudfront.net/deploy.png)](https://repocloud.io/details/?app_id=29)

      </details>

## ☁️ Aethon Labs Cloud

[Get Started with Aethon Labs Cloud](https://Aethon Labsai.com/)

## 🙋 Support

Feel free to ask any questions, raise problems, and request new features in [discussion](https://github.com/Aethon LabsAI/Aethon Labs/discussions)

## 🙌 Contributing

Thanks go to these awesome contributors

<a href="https://github.com/Aethon LabsAI/Aethon Labs/graphs/contributors">
<img src="https://contrib.rocks/image?repo=Aethon LabsAI/Aethon Labs" />
</a>

See [contributing guide](CONTRIBUTING.md). Reach out to us at [Discord](https://discord.gg/jbaHfsRVBW) if you have any questions or issues.
[![Star History Chart](https://api.star-history.com/svg?repos=Aethon LabsAI/Aethon Labs&type=Timeline)](https://star-history.com/#Aethon LabsAI/Aethon Labs&Date)

## 📄 License

Source code in this repository is made available under the [Apache License Version 2.0](LICENSE.md).
