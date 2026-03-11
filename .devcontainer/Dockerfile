FROM cirrusci/flutter:stable

# 安装额外工具
RUN apt-get update && apt-get install -y \
    curl \
    git \
    unzip \
    xz-utils \
    zip \
    libglu1-mesa \
    && rm -rf /var/lib/apt/lists/*

# 启用Web支持
RUN flutter config --enable-web

# 预下载常用包
RUN flutter precache

WORKDIR /workspaces/debt-planner
