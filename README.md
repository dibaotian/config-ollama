# config-ollama

#### edit the ollama configure file
#### #>sudo systemctl edit ollama.service

#### add the following, make ollama listen all ip and process parallel request
- [Service]
- Environment="OLLAMA_HOST=0.0.0.0" #设置服务监听的主机地址
- Environment="OLLAMA_NUM_PARALLEL=4" #并行处理请求的数量
- Environment="OLLAMA_MAX_LOADED_MODELS=4" #同时加载的模型数量

#### reload
#### #>sudo systemctl daemon-reload
#### #>sudo systemctl restart ollama
