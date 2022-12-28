### FastAPI

* FastAPI is a web framework for building APIs and is at par with **NodeJS** and **Go**. It is a **modern framework**  for building REST APIs . It's fast, easy to use and easy to learn.

*  FastAPI is way faster than many other web frameworks, not just that it’s also one of the fastest python modules out there.
-   FastAPI provides an easier implementation for Data Validation to define the specific data type of the data you send.

-   Automatic Docs to call and test your API(Swagger UI and Redoc).

-   FastAPI comes with built-in support for Asyncio, GraphQL and Websockets.

The simplest FastAPI file could look like this:

```py
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def root():
    return {"message": "Hello World"}
```

```bash
uvicorn main:app --reload  
INFO: Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)  
INFO: Started reloader process [28720]  
INFO: Started server process [28722]  
INFO: Waiting for application startup.  
INFO: Application startup complete.
```

* About the Object Detection Model
  * Yolov5 custom object detector built using - https://colab.research.google.com/drive/1gDZ2xcTOgR39tGGs-EZ6i3RTs16wmzZQ
  * Dataset from roboflow - https://public.roboflow.com/object-detection/aquarium
  * Yolov5 repo - [https://github.com/ultralytics/yolov5](https://github.com/ultralytics/yolov5)

* Testing the API -

![Screenshot_20221227_202758](/uploads/0625bc836f6048888050b45a2a864d3f/Screenshot_20221227_202758.png)

  * Test Image - 

![image](/uploads/9923b5b24b9f164114d3a926b8fa22d5/image.png)

![Screenshot_20221227_211557](/uploads/7b7a7275c1b6730dcdd93e5a04f6e42d/Screenshot_20221227_211557.png)

![Screenshot_20221227_211615](/uploads/42b3128a6a0ede7e0cfcd502590c7d7a/Screenshot_20221227_211615.png)

* Here is the complete json object returned by the request - 

```json
{
  "result": [
    {
      "xmin": 522.9768676758,
      "ymin": 67.446395874,
      "xmax": 629.4301757812,
      "ymax": 114.4814605713,
      "confidence": 0.7548267245,
      "class": 0,
      "name": "fish"
    },
    {
      "xmin": 447.186340332,
      "ymin": 13.4524745941,
      "xmax": 575.827331543,
      "ymax": 73.1524429321,
      "confidence": 0.716540575,
      "class": 0,
      "name": "fish"
    },
    {
      "xmin": 329.4973754883,
      "ymin": 31.7307434082,
      "xmax": 497.693359375,
      "ymax": 129.900177002,
      "confidence": 0.6890055537,
      "class": 0,
      "name": "fish"
    },
    {
      "xmin": 556.1241455078,
      "ymin": 230.778717041,
      "xmax": 738.9200439453,
      "ymax": 299.59765625,
      "confidence": 0.6510511637,
      "class": 4,
      "name": "shark"
    },
    {
      "xmin": 234.1691894531,
      "ymin": 532.2294311523,
      "xmax": 484.3969116211,
      "ymax": 619.7105102539,
      "confidence": 0.6352905631,
      "class": 4,
      "name": "shark"
    },
    {
      "xmin": 460.0694885254,
      "ymin": 69.7494354248,
      "xmax": 550.9253540039,
      "ymax": 132.159866333,
      "confidence": 0.5183494687,
      "class": 0,
      "name": "fish"
    }
  ]
}

```
