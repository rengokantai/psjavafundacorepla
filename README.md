#### psjavafundacorepla
######72 Multithreading and concurrency
```
ExecutorService es = Executors.newFixedThreadPool(3);
for(int i=0;i<infiles.length;i++){
  Adder adder = new Adder(..);
  es.submit(adder);
}
try{
  es.shutdown();
  es.awaitTermination(60,TimeUnit.SECONDS);
}catch(Exception e){
}
