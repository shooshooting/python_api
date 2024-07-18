Python API   

Structure:  

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


Using Podman  


Build the container image:  
podman build -t python_api -f Podmanfile .  

Run the container:  
podman run -d -p 8000:8000 python_api  

Access the API endpoint:  
curl http://localhost:8000/api/data  


Running Tests:  
pytest  
