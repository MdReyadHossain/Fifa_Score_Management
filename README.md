
# Strike Score

Strike Score is an ASP .NET Core MVC application designed to manage and track soccer tournament scores like FIFA. This system facilitates the organization and administration of tournaments by providing distinct functionalities for different user roles: Admin, Moderator, and User.

## Tournament Score System

The tournament is divided into two stages:
1. **Group Stage**: Teams are divided into groups where they play against each other. Points are awarded as follows:
   - Win: 3 points
   - Draw: 1 point
   - Loss: 0 points
   The top two teams from each group advance to the knockout stage based on points.

2. **Knockout Stage**: The top teams from the group stage compete in single-elimination matches. The winner of each match advances to the next round until a champion is crowned.

## User Roles and Functionalities

### Admin
- **Login**: Admin can log into the system.
- **Create Tournament**: Admin can create new tournaments by providing the tournament name.
- **Manage Tournament**: Admin can update all tournament details including teams, matches, and stadiums.
- **Switch Tournament**: Admin can switch between different tournaments by select from the tournament table.

### Moderator
- **Login**: Moderator can log into the system.
- **Manage Matches**: Moderator can update match details but cannot create new tournaments or modify the tournament schedule.
- **Switch Tournament**: Moderators can switch to view and manage different tournaments.

### User
- **View Scores**: Users can view the scores and standings of tournaments but cannot make any modifications.

## Features

- **Dynamic Database Creation**: When a new tournament is created, a corresponding database is generated with predefined tables.
- **Tournament Switching**: The system allows switching between different tournaments, updating the connection string to access the relevant database.
- **Role-Based Access Control**: Distinct functionalities are provided based on user roles to ensure secure and appropriate access.
- **User Interaction**: When a user watching the score, system will save the ip-address of this user for track of traffic.

## Installation and Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/MdReyadHossain/Strike_Score.git
    ```

2. Navigate to the project directory:
    ```bash
    cd Strike_Score
    ```

3. Restore dependencies:
    ```bash
    dotnet restore
    ```

4. Update the database connection string in `appsettings.json`:
    ```json
    "ConnectionStrings": {
      "DefaultConnection": "Server=.; Database=Strike_Score; Trusted_Connection=True; TrustServerCertificate=True;"
    }
    ```

5. Run the application:
    ```bash
    dotnet run
    ```

## Database Structure
![strike_score db diagram](https://i.postimg.cc/g2yRJDgj/Strike-Score-dbdiag.png)


## Contribution

1. Fork the repository.
2. Create a new branch:
    ```bash
    git checkout -b feature-branch
    ```
3. Commit your changes:
    ```bash
    git commit -m 'Add some feature'
    ```
4. Push to the branch:
    ```bash
    git push origin feature-branch
    ```
5. Open a pull request.

---

For more information, please contact through [reyadhosen@gmail.com](mailto:reyadhosen@gmail.com).
