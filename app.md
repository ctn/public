*Note: to view these diagrams, install [this Chrome plugin](https://chrome.google.com/webstore/detail/plantuml-visualizer/ffaloebcmkogfdkemcekamlmfkkmgkcf).*

### Model–System (Data Scientist–Software Engineer) Collaboration
```
@startuml
allowmixing
class App
Actor "Software Engineer" as SWE
Actor "Data Scientist" as DS
App ..> "AppModel" : uses
AppModel ..> Model
@enduml
```

