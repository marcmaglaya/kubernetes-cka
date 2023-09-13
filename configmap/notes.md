# IMPERATIVE : create confimap 
  kubectl create configmap <cm_name> --from-literal=<key>=<value>
  multiple : 

  kubectl create configmap <cm_name> --from-literal=<key>=<value> \
                                      --from-literal=<key>=<value> \
                                      --from-literal=<key>=<value>

# from file 
  kubectl create configmap <cm_name> --from-file=<filename>
  kubectl create configmap <cm_name> --from-file=app_config.properties

APP_COLOR: blue
APP_MODE: prod

# DECLARATIVE
