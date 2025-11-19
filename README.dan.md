# Ollama

## Installation

### From ~

```
curl -fsSL https://ollama.ai/install.sh | sh
sudo service ollama stop
sudo systemctl disable ollama.service
OLLAMA_HOST=0.0.0.0 ollama serve
ollama pull qwen3:0.6b
ollama pull qwen3:4b
ollama pull qwen3:8b
```

### From ~/repos/localGPT/

```
python3 -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
npm install
```

## Running

```
OLLAMA_HOST=0.0.0.0 ollama serve
```

```
. .venv/bin/activate
python run_system.py
```

## Monitoring

```
tail -f logs/*.log
```

## Remote access

`ssh -R 3000:localhost:3000 -R 8000:localhost:8000 -R 8001:localhost:8001 client_hostname`

## Memory tweaks

See [api_reference.md](./Documentation/api_reference.md)

## Custodial

```
echo "" > backend/chat_data.d
```
