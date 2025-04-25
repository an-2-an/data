---
Django ER Diagram
---
erDiagram
    User {
        AutoField id
        CharField password
        DateTimeField last_login
        BooleanField is_superuser
        CharField username
        CharField first_name
        CharField last_name
        CharField email
        BooleanField is_staff
        BooleanField is_active
        DateTimeField date_joined
    }
    UserProfile {
        BigAutoField id
        OneToOneField user
        FileField img
        IntegerField num_games
        FloatField won_games_ratio
    }
    Command {
        BigAutoField id
        ForeignKey game
        BooleanField is_winner
        DateTimeField created
        DateTimeField updated
        ManyToManyField players
    }
    Game {
        BigAutoField id
        DateTimeField created
        DateTimeField updated
    }
    Couple {
        BigAutoField id
        ForeignKey player1
        ForeignKey player2
        IntegerField num_games
        FloatField weight
    }

    UserProfile ||--|| User : user
    Command }|--|| Game : game
    Command }|--|{ User : players
    Couple }|--|| User : player1
    Couple }|--|| User : player2
    %% Размеры диаграммы и ориентация
    classDiagram
        direction TB
        classDiagram::theme dark
