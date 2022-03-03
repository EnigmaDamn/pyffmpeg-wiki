
## Properties

* **report_progress**: _bool_ [Default: True]

    This should be set before progress will be captured

* **onProgressChanged**: _def(progres: int)_ [Default: progressChangeMock]

This should be set to a name of a function/method. It will be called whenever progress changes. The progress will be passed to the function/method as an int