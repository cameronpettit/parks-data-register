# Parks Data Registry API 

# Root

### Root GET
```
GET /
```
Not implemented.

# Parks

### GET all parks information
```
GET /parks
```
Not implemented.

### GET specific park information
```
GET /parks/{identifier}
```
Not implemented.

**Path Parameters:**
- `identifier` (number): The unique park identifier (ParkID/ORCS)

##	Park Names

### GET all parks names information
```
GET /parks/names
```
Partially implemented. Must be supplied with at least one required query parameter: `status` or `legalName`.

**Query Parameters**
- `status` (string) - the status of the park name object. To get the current park name list, use `status=current`.
- `legalName` (string) - the legal name of the park name object. The search is for an exact string match and respects letter casing.

**Examples:**
- Get a list of the current names for all parks:
```
GET apiUrl/parks/names?status=current
```
- Search park names for legal name 'Strathcona Park':
```
GET apiUrl/parks/names?legalName=Strathcona Park
```
- Search current park names for legal name 'Strathcona Park':
```
GET apiUrl/parks/names?status=current&legalName=Strathcona Park
```

### GET specific park name information
```
GET /parks/{identifier}/name
```
Get all the name data belonging to a park (identified by ParkID).

**Path Parameters:**
- `identifier` (number): The unique park identifier (ParkID/ORCS)

**Query Parameters**
- `status` (string): the status of the park name object. To get the current park name, use `status=current`.

**Examples:**
- Get all name information for Strathcona Park (ParkID = 1):
```
GET apiUrl/parks/1/name
```
- Get current name for Strathcona Park (ParkID = 1):
```
GET apiUrl/parks/1/name?status=current
```


