
# VirusTotal API

The VirusTotal API allows you to search for file hashes in the VirusTotal database and get the results as a JSON response.

## Usage

To use the VirusTotal API, send a GET request to the following URL, replacing `QUERY` with the file hash you want to search for:

`https://api.pawan.krd/security/virustotal?q=QUERY` 

## Parameters

-   `q`: (required) the URL, IP address, domain, or file hash to search for

## Response

The API will return a JSON object with the following properties:

-   `status`: a boolean indicating whether the query was successful
-   `result`: an object containing the following properties:
    -   `query`: the query string that was searched for
    -   `info`: an object containing information about the query, such as the SHA256 hash, filename, and detection ratio
    -   `securityVendors`: an array of objects containing information about the security vendors that detected the query as malicious, including the security vendor name, result, update date, and whether it was detected as malicious

## Example

To search for the file hash `62d3624992cf0009d29291d5341902d4`, send the following request:

GET [https://api.pawan.krd/security/virustotal?q=62d3624992cf0009d29291d5341902d4](https://api.pawan.krd/security/virustotal?q=62d3624992cf0009d29291d5341902d4)

