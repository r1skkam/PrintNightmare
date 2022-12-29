# TryHackMe | PrintNightmare
[PrintNightmare](https://tryhackme.com/room/printnightmarehpzqlp8)

```Learn about the vulnerability known as PrintNightmare (CVE-2021-1675) and (CVE-2021-34527)```

![image](https://user-images.githubusercontent.com/58542375/209743560-206d44ab-5918-4c54-aea3-34898eecd6a1.png)

## Task 6 Detection: Windows Event Logs
![image](https://user-images.githubusercontent.com/58542375/209743956-fa1301db-2be0-414c-904c-25f909a6999f.png)
![image](https://user-images.githubusercontent.com/58542375/209743996-2ad5adc1-e244-4f13-a2b9-a548540c3293.png)

```Event Viewer > Applications and Services Logs > Microsoft > Windows > PrintService > Admin```

![image](https://user-images.githubusercontent.com/58542375/209744266-04fdae7a-5cec-4f62-b916-819eca7ca42d.png)
![image](https://user-images.githubusercontent.com/58542375/209744456-a49f4210-4b81-4f42-b0b5-8a31d8fe2d4b.png)

```%SystemRoot%\System32\Winevt\Logs\Microsoft-Windows-PrintService%4Admin.evtx```

```Log Name:      Microsoft-Windows-PrintService/Admin
Source:        Microsoft-Windows-PrintService
Date:          8/13/2021 10:33:40 AM
Event ID:      808
Task Category: Initializing
Level:         Error
Keywords:      Print Spooler
User:          SYSTEM
Computer:      Finance-01.THMdepartment.local
Description:
The print spooler failed to load a plug-in module C:\Windows\system32\spool\DRIVERS\x64\3\svch0st.dll, error code 0x45A. See the event user data for context information.
Event Xml:
<Event xmlns="http://schemas.microsoft.com/win/2004/08/events/event">
  <System>
    <Provider Name="Microsoft-Windows-PrintService" Guid="{747ef6fd-e535-4d16-b510-42c90f6873a1}" />
    <EventID>808</EventID>
    <Version>0</Version>
    <Level>2</Level>
    <Task>36</Task>
    <Opcode>12</Opcode>
    <Keywords>0x8000000000020000</Keywords>
    <TimeCreated SystemTime="2021-08-13T17:33:40.312868200Z" />
    <EventRecordID>3</EventRecordID>
    <Correlation />
    <Execution ProcessID="2244" ThreadID="6744" />
    <Channel>Microsoft-Windows-PrintService/Admin</Channel>
    <Computer>Finance-01.THMdepartment.local</Computer>
    <Security UserID="S-1-5-18" />
  </System>
  <UserData>
    <LoadPluginFailed xmlns="http://manifests.microsoft.com/win/2005/08/windows/printing/spooler/core/events">
      <PluginDllName>C:\Windows\system32\spool\DRIVERS\x64\3\svch0st.dll</PluginDllName>
      <ErrorCode>0x45a</ErrorCode>
      <Context>112</Context>
    </LoadPluginFailed>
  </UserData>
</Event>```

![image](https://user-images.githubusercontent.com/58542375/209936244-88e8b19b-a497-4a7d-9e47-7f39bb3f6b8a.png)
![image](https://user-images.githubusercontent.com/58542375/209936347-ca29eb6c-015c-48b3-bcd2-b11c7d4bf1b7.png)

