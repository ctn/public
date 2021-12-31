*Note: to view these diagrams, install [this Chrome plugin](https://chrome.google.com/webstore/detail/plantuml-visualizer/ffaloebcmkogfdkemcekamlmfkkmgkcf).*

### Model–System (Data Scientist–Software Engineer) Collaboration
```
@startuml
allowmixing

 
class App {
  in apps/app.py
}

class AppModel #lightgreen {
  in models/app_model.py
}

class Model {
  in models/model.py
}

App ..> AppModel : uses
AppModel ..> Model : embeds
AppModel : process()
AppModel : predict()

Actor "Software Engineer" as SWE
Actor "Data Scientist" as DS
SWE .right.> App : maintains
DS .right.> Model : maintains


note right of AppModel
  Do not modify the name of this class,
  so that DS and SWE can move 
  independently of each other.
end note

note right of Model
  Can be any class as determined by DS
end note
@enduml
```

