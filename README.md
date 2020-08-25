# nomad-demo-0
Nomad 101 follow the learn path notes

# Testing official learning 

From : https://learn.hashicorp.com/tutorials/nomad/get-started-run?in=nomad/get-started

# Error 1 

When running :  `sudo nomad agent -dev` getting :

```bash
=> Error starting http server: failed to start HTTP listener: listen tcp 127.0.0.1:4646: bind: address already in use
```

In parrallel, there is also JDK error : 

> To us the "java" command-line tool you need to install a JDK

That pop-ups every ..mnute or so, very annoying. 

so, the Vagrant setup is optional... :-( 

# Notes for manual update

1. On MacOS you going to need JDK, otherwise the error about java command line binary going to pop up every minute
2. There is not Consul error at least for Nomad   Version: 0.12.3 when starting in agent mode. Opposite to whats mentioned in manual : https://learn.hashicorp.com/tutorials/nomad/get-started-run?in=nomad/get-started
3. No, we don't need to specify any names of the task, ID is enough e.g. this : `nomad alloc logs 8ba85cef redis` is overkill, just this : `nomad alloc logs 8ba85cef` is enough, shorter, simplier. Produces equal results
4. On MacOS : With default Docker engine 19.03.12 ( installation as Docker desktop) we need to starte agents `without sudo` , or they will fail to mount required folders. Or , modify exampel/folders mounts. 

