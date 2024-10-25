
# MovieLensALS - Movie Recommendation System

This project implements a movie recommendation system using the ALS (Alternating Least Squares) algorithm with the MovieLens dataset. The system loads movie rating data, processes it, and outputs movie recommendations. Results are stored both in the application and in MySQL for persistence.

## Project Structure

```
MovieLensALS
├── pom.xml
└── src
    └── main
        └── recommend
            ├── MovieLensALS.scala     
            ├── InsertIntoMySQL.scala    
            ├── ReadFromMySQL.scala     
            └── DeleteFromMySQL.scala  
```

## Dataset

Data is sourced from `movie_recommend.zip`, containing:
- **ratings.dat**: User ratings dataset
- **personalRatings.txt**: Sample ratings dataset for testing
- **movies.dat**: Movie dataset with movie metadata

## Setup and Configuration

1. **Scala SDK**: Ensure Scala SDK version 2.11.8 is installed in IntelliJ IDEA.
2. **Data Loading**: Use [Kettle](https://community.hitachivantara.com/docs/DOC-1009853) to load the dataset files into HDFS.
3. **Dependencies**: Specify project dependencies in `pom.xml` to match required versions of libraries.

## Running the Movie Recommendation System

1. **Load Data and Run MovieLensALS.scala**:
   - Execute the `MovieLensALS.scala` script in IntelliJ IDEA. This will generate movie recommendations for users based on the ALS model.

2. **Results**:
   - Recommended movie information will display in the console.
   - Results are stored in the MySQL database.

3. **Data Persistence with MySQL**:
   - The following scripts handle database operations:
     - **InsertIntoMySQL.scala**: Stores recommendation results in MySQL.
     - **ReadFromMySQL.scala**: Retrieves stored recommendations.
     - **DeleteFromMySQL.scala**: Removes specified data from the database.

## Packaging the Application

1. **Build JAR**:
   - In IntelliJ IDEA, use the packaging tool to compile and bundle the project into an executable JAR file.
   - The packaged JAR can be deployed or distributed for execution on other systems.

