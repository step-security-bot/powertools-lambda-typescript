# See here for image contents: https://github.com/microsoft/vscode-dev-containers/blob/v0.212.0/containers/javascript-node/.devcontainer/base.Dockerfile
FROM mcr.microsoft.com/vscode/devcontainers/javascript-node@sha256:ff7fcaf39a616aed41b7e9af6ebedfee1c605e89ba9416c6fa79f33762345aa7

# Install fnm to manage Node.js versions
RUN curl -fsSL https://fnm.vercel.app/install -o /tmp/install \
  && chmod a+x /tmp/install \
  && /tmp/install \
  && rm /tmp/install

# Install AWS SAM CLI
RUN curl -LO https://github.com/aws/aws-sam-cli/releases/latest/download/aws-sam-cli-linux-x86_64.zip \
  && unzip -q aws-sam-cli-linux-x86_64.zip -d sam-installation \
  && sudo ./sam-installation/install \
  && rm -rf sam-installation aws-sam-cli-linux-*