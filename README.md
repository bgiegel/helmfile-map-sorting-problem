# helmfile-map-sorting-problem

To reproduce the issue just run : 

```
cd helmfile_config
helmfile -e prod template
```

You will see that sometimes the output map is not always sorted in the same order.
Try to change the client_id fields in backupd.env.yaml with random string like abc, def, ghi 
and it will work and always return a map in the same order. Same for int values. But not with these specific strings...
