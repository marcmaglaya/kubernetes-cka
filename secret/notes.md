# IMPERATIVE : create secret 
  kubectl create secret generic <secret_name> --from-literal=<key>=<value>
  multiple : 

  kubectl create secret generic <secret_name> --from-literal=<key>=<value> \
                                      --from-literal=<key>=<value> \
                                      --from-literal=<key>=<value>

# from file 
  kubectl create secret generic <secret_name> --from-file=<filename>
  kubectl create secret generic <secret_name> --from-file=app_secret.properties

APP_COLOR: blue
APP_MODE: prod

# DECLARATIVE
