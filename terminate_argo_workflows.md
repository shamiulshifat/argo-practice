1. first install matching/ latest argo cli only from here:

https://github.com/argoproj/argo-workflows/releases/

then:
try : argo terminate <wf name>
  
  then it may gives this error:
  '''
  invalid configuration: no configuration has been provided, try setting KUBERNETES_MASTER environment variable
  '''
  
  to fix this:
  
  
