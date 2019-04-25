# server-swift

# Setting up the envirment

## Swift Package
```zsh
swift package init --type executable  
```


## Swift build
```zsh
swift build

## Swift package manager should include the dependencies in the target
```zsh
let package = Package(
    name: "server-swift",
    dependencies: [
        .package(url: "https://github.com/kylef-archive/Curassow.git", from: "0.6.0"),
    ],
    targets: [
        .target(
            name: "server-swift",
            dependencies: ["Curassow"])
     ]
)

## Builder docker
```zsh
docker build -t swift-server ./
```

## Docker run
```zsh
docker run -p 8000:8000 swift-server
```

## Make the compose file to seperate the db from the web application
```zsh
docker-compose.yml
```


## Build docker compose
```zsh
docker-compose build
```

## Run docker compose
```zsh
docker-compose up
```

## execute something docker compose
```zsh
docker exec -it swiftserver_db_1 psql -U postgres -d swift_talk
```



