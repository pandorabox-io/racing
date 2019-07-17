
# Racing mod for minetest

Create races and run them with multiple players (WIP/Proposal)

## Example

Player `HanSolo`:
```
/grantme racing_admin
/race_create Kessel_run
/race_add_waypoint Kessel_run Asteroid_1 100
/race_add_waypoint Kessel_run Big_Asteroid_2 250
/race_add_waypoint Kessel_run Small_Place 10
/race_prepare Kessel_run default:goldblock 99 true 60 300
```

Server message
```
* [Racing] Player "HanSolo" created a race "Kessel_Run" that starts in 60 seconds and rewards 99 default:goldblock!
```

Player `OtherDude`:
```
/race_join Kessel_run
```

Server message
```
* [Racing] Player "OtherDude" joined the race "Kessel_Run", there are 2 contestants now
```


## Reference

### Privileges

* `racing_admin` can edit races

### Chatcommands

#### /race_list

* privs: *none*

#### /race_create <race-name>

* privs: `racing_admin`

#### /race_delete <race-name>

* privs: `racing_admin`

#### /race_list_waypoints <race-name>

* privs: `racing_admin`

#### /race_add_waypoint <race-name> <waypoint-name> <radius>

* privs: `racing_admin`

#### /race_remove_waypoint <race-name> <waypoint-name>

* privs: `racing_admin`

#### /race_prepare <race-name> <reward-item> <reward-count> <announce> <start-in-seconds> <end-in-seconds>

* privs: `racing_admin`

#### /race_join <race-name>

* privs: *none*

#### /race_leave

* privs: *none*

#### /race_abort

* privs: `racing_admin`
