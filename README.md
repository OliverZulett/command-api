# Command API

A rest api build in .Net core framework 5.0.402.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.

```bash
pip install foobar
```

## Usage

```bash

# create docker volume
docker volume create sql-server

# create docker container
docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=myStrongPassword123" \
   -p 1433:1433 --name sql-server -h sql-server -v sql-server \
   -d mcr.microsoft.com/mssql/server:2019-latest

# install entityFramework
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
dotnet add package Microsoft.EntityFrameworkCore.Tools --version 1.1.0-msbuild3-fina
dotnet tool install --global dotnet-ef

# execute migration
dotnet ef migrations add AddCommandToDB

# update database
dotnet ef database update

# build api
dotnet build

# run api
dotnet run

#test
localhost:5001/api/commands/
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)