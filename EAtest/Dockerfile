# 使用基础镜像
FROM python:3.11

# 安装系统依赖库
RUN apt-get update && apt-get install -y \
    libpq-dev \
    build-essential

# 设置工作目录
WORKDIR /app

# 复制当前目录内容到工作目录
COPY . /app

# 打印Python版本
RUN python --version

# 打印pip版本
RUN pip --version

# 安装Python依赖并使用国内镜像源
RUN pip install --no-cache-dir -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

# 设置运行代码的命令
CMD ["python", "test.py"]
