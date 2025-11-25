# 使用輕量版 python 作為基底
FROM python:3.10-slim

# 設定工作目錄
WORKDIR /app

# 把 requirements.txt 複製進容器
COPY requirements.txt .

# 安裝 Python 套件
RUN pip install --no-cache-dir -r requirements.txt

# 把程式碼複製進容器
COPY . .

# 啟動 FastAPI 服務
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
