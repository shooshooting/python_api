
# Python API 


## Structure

```
python_api/
├── .pytest_cache/
├── api/
│   ├── __pycache__/
│   ├── __init__.py
│   ├── dataset.json
│   ├── main.py
│   └── test_main.py
├── Podmanfile
└── requirements.txt
```

- `requirements.txt`: List of dependencies required by the project.




## Running

### Podman


1. Build :

```sh
podman build -t python_api -f Podmanfile .
```

2. Run :

```sh
podman run -d -p 8000:8000 python_api
```

3. check logs:

```sh
podman logs <container_id>
```

4. endpoint:

```sh
curl http://localhost:8000/api/data
```

5. c's shell:

```sh
podman exec -it <container_id> /bin/sh
```


## Running Tests

```sh
pytest
```
