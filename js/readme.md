# OpenFaaS sample JS service

* initiate the project
```sh
faas-cli new js-test --lang node
```

* build and deploy locally
```sh
cd js
faas-cli build -f stack.yml
faas-cli push -f stack.yml
faas-cli deploy -f stack.yml --namespace dev

# OR

faas-cli up -f stack.yml -n dev
```

* invoke service
```sh
faas-cli invoke -f stack.yml js-test.dev
# OR
curl http://ofaas.kube.local.io/function/js-test.dev
```

* get list of services
```sh
faas-cli list -n dev
```

* remove service
```sh
faas-cli rm -n dev js-test
```