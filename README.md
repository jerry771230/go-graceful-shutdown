# go-graceful-shutdown

Graceful shutdown.

## Commands

### Run app

```bash
$ go run ./internal/main.go
```

## Taskfile

```bash
task --list
task: Available tasks for this project:
* build: 	Build the app
* run: 		Run the app
```

## Shutdown Error

In this case, you will receive an error message.

```pre
  router.GET("/", func(c *gin.Context) {
		time.Sleep(5 * time.Second)
		c.String(http.StatusOK, "Welcome Gin Server")
	})

  ...

  c, cancel := context.WithTimeout(context.Background(), 3*time.Second)
```

The error message will be: `Server Shutdown: context deadline exceeded`.

## Ref

- [[Go 教學] 什麼是 graceful shutdown?](https://blog.wu-boy.com/2020/02/what-is-graceful-shutdown-in-golang/)
- [[DAY29]Golang Graceful Shutdown優雅的關機(?)](https://ithelp.ithome.com.tw/articles/10249227)
