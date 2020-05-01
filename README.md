# about this chart

This is a HELM chart that I put together based on my converting Seatable's docker setup to something Kubernetes understands.

If you were to substitute the variables yourself and run `kubectl apply` you would end up with the same setup.

Feel free to create an issue if you try this chart and it doesn't work for you.

# values.yaml

So, what do you need to know about values.yaml?

I think most of it is self explanatory. With a couple exceptions:

Setting istio.enabled to true means that a certificate should be generated, provided you have configured a letsencrypt issuer.
A gateway and a virtual service will also be created.

Replicas: I would leave this number untouched as I do not expect Seatable to be happy with more than one instance of any service.

If you remove storage.class, the default storage class should be used.
