---
icon: hammer-brush
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# CedMod Api

These are all endpoints in the `CedMod api` and their current state in the project.

### Api

| Type                                                                                 | Api Endpoint                | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | --------------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/ApiTokens/Query`      | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a8e2183e-d2be-4188-9837-190b8d1dd020) | `/Api/ApiTokens/Add`        | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/ApiTokens/{id}`       | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/797e682e-896c-45a6-8710-67baf0caf424) | `​/Api​/ApiTokens​/{id}`    | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `​/Api​/ApiTokens​/{id}`    | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/ApiTokens/{id}/Token` | :x:                   | :x:            | :x:    | Not Implemented        |

### Appeals

| Type                                                                                 | Api Endpoint                    | Non Useronly Endpoint | Implementation       | Tested               | Implemented on Version |
| ------------------------------------------------------------------------------------ | ------------------------------- | --------------------- | -------------------- | -------------------- | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Appeal/GetBans`           | :x:                   | :x:                  | :x:                  | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a8e2183e-d2be-4188-9837-190b8d1dd020) | `/Api/Appeal/Submit`            | :x:                   | :x:                  | :x:                  | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Appeal/Query`             | :white\_check\_mark:  | :white\_check\_mark: | :x:                  | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/Appeal/{appealId}/Handle` | :white\_check\_mark:  | :white\_check\_mark: | :white\_check\_mark: | `0.3.0`                |

### AuditLogsController

| Type                                                                                 | Api Endpoint          | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | --------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/AuditLog/Query` | :grey\_question:      | :x:            | :x:    | `0.3.0`                |

### Ban

| Type                                                                                 | Api Endpoint                   | Non Useronly Endpoint | Implementation       | Tested               | Implemented on Version |
| ------------------------------------------------------------------------------------ | ------------------------------ | --------------------- | -------------------- | -------------------- | ---------------------- |
| ![](https://github.com/user-attachments/assets/4067d98b-db32-4b04-b284-7999075bb687) | `/Api/Ban/{banId}/AppealState` | :white\_check\_mark:  | :white\_check\_mark: | :white\_check\_mark: | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/4067d98b-db32-4b04-b284-7999075bb687) | `/Api/Ban/{banId}/Bypassable`  | :white\_check\_mark:  | :white\_check\_mark: | :x:                  | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/4067d98b-db32-4b04-b284-7999075bb687) | `/Api/Ban/{banId}/Duration`    | :white\_check\_mark:  | :white\_check\_mark: | :x:                  | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/4067d98b-db32-4b04-b284-7999075bb687) | `/Api/Ban/{banId}/Reason`      | :white\_check\_mark:  | :white\_check\_mark: | :x:                  | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/Ban/{banId}`             | :white\_check\_mark:  | :white\_check\_mark: | :x:                  | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/a8e2183e-d2be-4188-9837-190b8d1dd020) | `/Api/Ban/Issue`               | :white\_check\_mark:  | :white\_check\_mark: | :x:                  | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/api/Ban/Query`               | :white\_check\_mark:  | :white\_check\_mark: | :x:                  | `0.3.0`                |

### Banlist

| Type                                                                                 | Api Endpoint             | Non Useronly Endpoint | Implementation       | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ------------------------ | --------------------- | -------------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Banlist/Query`     | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/Banlist/{id}`      | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/797e682e-896c-45a6-8710-67baf0caf424) | `/Api/Banlist/{id}/{id}` | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |

### BanLog

| Type                                                                                 | Api Endpoint          | Non Useronly Endpoint | Implementation       | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | --------------------- | --------------------- | -------------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/BanLog/User`    | :x:                   | :x:                  | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/BanLog/{banId}` | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Changelog/Get`  | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |

### Changelog

| Type                                                                                 | Api Endpoint         | Non Useronly Endpoint | Implementation       | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | -------------------- | --------------------- | -------------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Changelog/Get` | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |

### Config

| Type                                                                                 | Api Endpoint      | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ----------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Config/Get` | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/Config/Set` | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Config/Set` | :x:                   | :x:            | :x:    | Not Implemented        |

### ExternalLookup

| Type                                                                                 | Api Endpoint                 | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ---------------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/v3/Lookup`             | :grey\_question:      | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/v3/LookupAuthCallback` | :grey\_question:      | :x:            | :x:    | Not Implemented        |

### Feedback

| Type                                                                                 | Api Endpoint           | Non Useronly Endpoint | Implementation       | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ---------------------- | --------------------- | -------------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a8e2183e-d2be-4188-9837-190b8d1dd020) | `/Api/Feedback/Submit` | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |

### Instance

| Type                                                                                 | Api Endpoint            | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ----------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Instance/Icon`    | :grey\_question:      | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Instance/Initial` | :grey\_question:      | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Instance/Stats`   | :grey\_question:      | :x:            | :x:    | Not Implemented        |

### Login

| Type                                                                                 | Api Endpoint                | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | --------------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Login/InitiateLogin`  | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a8e2183e-d2be-4188-9837-190b8d1dd020) | `/Api/Login/ServerCallback` | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Login/ClientCallback` | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Login/LoginConfirm`   | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Login/LogoutConfirm`  | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Login/Check`          | :x:                   | :x:            | :x:    | Not Implemented        |

### Mute

| Type                                                                                 | Api Endpoint                 | Non Useronly Endpoint | Implementation       | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ---------------------------- | --------------------- | -------------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/4067d98b-db32-4b04-b284-7999075bb687) | `/Api/Mute/{banId}/Type`     | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/4067d98b-db32-4b04-b284-7999075bb687) | `/Api/Mute/{banId}/Duration` | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/4067d98b-db32-4b04-b284-7999075bb687) | `/Api/Mute/{banId}/Reason`   | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/Mute/{banId}`          | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/a8e2183e-d2be-4188-9837-190b8d1dd020) | `/Api/Mute/Issue`            | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Mute/Query`            | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |

### MuteLog

| Type                                                                                 | Api Endpoint           | Non Useronly Endpoint | Implementation       | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ---------------------- | --------------------- | -------------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/MuteLog/{banId}` | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/MuteLog/User`    | :x:                   | :x:                  | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/MuteLog/Query`   | :white\_check\_mark:  | :white\_check\_mark: | :x:    | `0.3.0`                |

### Permissions

| Type                                                                                 | Api Endpoint           | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ---------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Permissions/Get` | :grey\_question:      | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/Permissions/Set` | :grey\_question:      | :x:            | :x:    | Not Implemented        |

### Player

| Type                                                                                 | Api Endpoint                       | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ---------------------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Player/{playerId}/StatsUser` | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Player/{UserId}/User`        | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Player/{playerId}/Stats`     | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Player/Query`                | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Player/ResetStaff/{userId}`  | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |

### QueryServer

| Type                                                                                 | Api Endpoint                     | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | -------------------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/QueryServer/Query`         | :grey\_question:      | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a8e2183e-d2be-4188-9837-190b8d1dd020) | `/Api/QueryServer/Create`        | :grey\_question:      | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/QueryServer/{id}`          | :grey\_question:      | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/797e682e-896c-45a6-8710-67baf0caf424) | `/Api/QueryServer/{id}`          | :grey\_question:      | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/QueryServer/{id}/Settings` | :grey\_question:      | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/QueryServer/{id}/Settings` | :grey\_question:      | :x:            | :x:    | Not Implemented        |

### ReportController

| Type                                                                                 | Api Endpoint        | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Report/User`  | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Report/Query` | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |

### RoleSync

| Type                                                                                 | Api Endpoint              | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ------------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/RoleSync/GetStatus` | :x:                   | :x:            | :x:    | Not Implemented        |

### Stafflist

| Type                                                                                 | Api Endpoint           | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ---------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Stafflist/Query` | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |

### TeamkillLogs

| Type                                                                                 | Api Endpoint                    | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ------------------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/TeamkillLogs/Query`       | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/TeamkillLogs/{id}`        | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/TeamkillLogs/Viewer/{id}` | :grey\_question:      | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/TeamkillLogs/Rooms/{id}`  | :grey\_question:      | :x:            | :x:    | Not Implemented        |

### Translation

| Type                                                                                 | Api Endpoint                          | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ------------------------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Translation/GetTranslation`     | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Translation/GetTranslationDate` | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Translation/Get/{languageCode}` | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Translation/List`               | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/Translation/Set/{languageCode}` | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Translation/ListPublic`         | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Translation/SetUser/{langCode}` | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |

### User

| Type                                                                                 | Api Endpoint                    | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ------------------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/User/CheckSteam`          | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a8e2183e-d2be-4188-9837-190b8d1dd020) | `/Api/User/SetSteam/{steamid }` | :x:                   | :x:            | :x:    | Not Implemented        |

### UserPreferences

| Type                                                                                 | Api Endpoint               | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | -------------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/UserPreferences/Get` | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/UserPreferences/Set` | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |

### Warn

| Type                                                                                 | Api Endpoint               | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | -------------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/4067d98b-db32-4b04-b284-7999075bb687) | `/Api/Warn/{banId}/Reason` | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/Warn/{banId}`        | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Warn/User`           | :x:                   | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Warn/Query`          | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a8e2183e-d2be-4188-9837-190b8d1dd020) | `/Api/Warn/Issue`          | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |

### Watchlist

| Type                                                                                 | Api Endpoint                  | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ----------------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Watchlist/Query`        | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/watchlist/{id}`         | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Watchlist/Group/{id}`   | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a8e2183e-d2be-4188-9837-190b8d1dd020) | `/Api/Watchlist/Issue`        | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/4067d98b-db32-4b04-b284-7999075bb687) | `/Api/Watchlist/Edit`         | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/Watchlist/Delete`       | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a8e2183e-d2be-4188-9837-190b8d1dd020) | `/Api/Watchlist/Group/Issue`  | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/4067d98b-db32-4b04-b284-7999075bb687) | `/Api/Watchlist/Group/Edit`   | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/Watchlist/Group/Delete` | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |

### Whitelists

| Type                                                                                 | Api Endpoint            | Non Useronly Endpoint | Implementation | Tested | Implemented on Version |
| ------------------------------------------------------------------------------------ | ----------------------- | --------------------- | -------------- | ------ | ---------------------- |
| ![](https://github.com/user-attachments/assets/a6e32603-d14e-4349-8858-ec892db67c39) | `/Api/Whitelists/Query` | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/a8e2183e-d2be-4188-9837-190b8d1dd020) | `/Api/Whitelists/New`   | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/639a0a7d-cdb3-43ae-9957-cb92ad322fbc) | `/Api/Whitelists/{id}`  | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
| ![](https://github.com/user-attachments/assets/797e682e-896c-45a6-8710-67baf0caf424) | `/Api/Whitelists/{id}`  | :white\_check\_mark:  | :x:            | :x:    | Not Implemented        |
