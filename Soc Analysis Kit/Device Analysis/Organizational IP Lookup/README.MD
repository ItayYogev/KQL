# Organizational IP Lookup
This query retrieves network events from the DeviceNetworkEvents table, filtering for a specified remote IP address. it provides a chronological view of all network interactions associated with that IP.

The purpose of this query is to facilitate the investigation of potential security incidents linked to a particular IP address. By focusing on a specific remote IP, analysts can identify unusual or malicious activities, such as unauthorized access attempts or data exfiltration.

![Screenshot](https://github.com/user-attachments/assets/68874edb-e4f3-469c-a04c-04fc2fb773da)

If you want to limit the search to a specific PC, you can add this line to the query:
```sh
where DeviceName =~ "Device Name will be here" // enter the device name here
```