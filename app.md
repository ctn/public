*Note: to view these diagrams, install [this Chrome plugin](https://chrome.google.com/webstore/detail/plantuml-visualizer/ffaloebcmkogfdkemcekamlmfkkmgkcf).*

### Model–System (Data Scientist–Software Engineer) Collaboration
```
@startuml
allowmixing
class App
Actor SWE
Actor "Data Scientist"
App ..> "AppModel" : uses
AppModel ..> Model
@enduml
```

