# Log-File-Parser

## Usage

```sh
log-file-parser.jar <text-input-file> <json-output-file>
```

## Input file format

```txt
2019-01-07_16:13:03 Example_Thermostat actuator: 10
2019-01-07_16:13:03 Example_Thermostat battery: ok
2019-01-07_16:13:03 Example_Thermostat batteryLevel: 3
2019-01-07_16:13:03 Example_Thermostat desired-temp: 17.5
2019-01-07_16:13:03 Example_Thermostat measured-temp: 17.9
2019-01-07_16:13:03 Example_Thermostat motorErr: ok
2019-01-07_16:15:51 Example_Thermostat actuator: 10
2019-01-07_16:15:51 Example_Thermostat battery: ok
2019-01-07_16:15:51 Example_Thermostat batteryLevel: 3
2019-01-07_16:15:51 Example_Thermostat desired-temp: 17.0
2019-01-07_16:15:51 Example_Thermostat measured-temp: 17.8
2019-01-07_16:15:51 Example_Thermostat motorErr: ok
```

## Output file format

```json
{
    "Example_Thermostat": [
        {"date": "1546877583", "measured": 17.5, "desired": 17.5},
        {"date": "1546877751", "measured": 17.8, "desired": 17.0}
    ]
}
```