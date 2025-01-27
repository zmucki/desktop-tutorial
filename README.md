# Update t1
# Anna is the best
# Peter is the best boss
# Vin is t

another update


# Proposed-BuildingBlocks

Landing page for all proposed building blocks; use the README to navigate through all the Building Blocks.

## Implementation of new BBs

- New BB should be implemented using the [BB_Template](/utils/BB_Template.md).  
- If you create a folder without content, put a .gitkeep into the folder.  
- Whitespaces in Folders: "-" (Dash)  
- Whitespaces in Files: "_" (Underscore)  

Abbreviations have to be added to the [abbreviation list](/utils/Abbreviations.md).

When a new BB or folder is added to the libary, the structure in the README can be updated using 
the [README Generator](/scripts/readme_generator.py). To adjust contents of the README other than 
the Navigation, change them in the [README_base file](/utils/README_base.md). The Navigation will 
be inserted at the "## Navigation" flag in the [README_base file](/utils/README_base.md).

> [!CAUTION]
> If you don't follow the structure correctly the automatic structure generation will not work!

### Automatic README generation

The README gets automatically updated when changes of the folder structure or [README_base file](/utils/README_base.md) are pushed to a branch and when a pull request is merged to the main branch. test!!!!!!!!!!!!!!!!!

> [!Warning]
>If your github account was created before July 18, 2017, automatic creation of the README will not work. Please update the README maually by running the readme_generator.py file and creating a pull request to the main branch"

### Folder Structure

When implementing a new BB one has to comply to the following folder structure:

```
📁library
    └──📁In-Vehicle
        └── 📁BB-SC  # primary tag
            └── readme.md  
            └── 📁AppLayer  # layer (AppLayer, MWLayer, OSLayer, HWLayer)
                └── readme.md  
                └── 📁Communication  # functional cluster name
                    └── BB_AOSP_Push_Notification_Service.md  # BB - if it is in >1 FC or tag, put symlink there
                    └── 📁BB_OTA_Manager  # folder if more than a .md file exists for BB
                        └── BB_OTA_Manager.md # BB if it is in >1 FC or tag, put symlink there
                        └── BB_OTA_Manager.xml 

```

## BB Tags

First tag of BB defines its location in git repo

|Tag|Description|
|----|----|
|BB-SC|Building Block Stack Component (In-Vehicle / On-Board)|
|BB-CSC|Building Block Cloud Stack Component (Cloud / Off-Board)|
|BB-MU|Building Block Mockup Unit (In-Vehicle / On-Board Component)|
|BB-CMU|Block Cloud Mockup Unit (Cloud / Off-Board Component)|
|BB-EST|Building Block Engineering & Support Tools (for In-Vehicle / On-Board Components)|
|BB-CEST|Building Block Cloud Engineering & Support Tools (for Cloud / Off-Board Components)|
|S-BB|Supporting Building Blocks (Standards, API & Interface Definitions, standardized Data Model)|
|FC|Functional Cluster – Logical group of technically similar BBs|
|BB-SC-TC|Building Block Stack Component ToolChain (contains compatible set of Engineering & Support Tools and Mockup Units for In-Vehicle dev)|
|BB-CSC-TC|Building Block Cloud Stack Component ToolChain ToolChain (contains compatible set of Engineering & Support Tools and Mockup Units for Cloud dev)|
|BB-WE|Whatever Tag / Whitecard|

## Navigation
- library
    - [test](/library/test/test.md)
    - unsorted_BB
        - Daniel
            - [BB_Template_filled_FleetData_WP3](/library/unsorted_BB/Daniel/BB_Template_filled_FleetData_WP3.md)
            - [BB_Template_filled_RemoteVehicleInteraction_WP3](/library/unsorted_BB/Daniel/BB_Template_filled_RemoteVehicleInteraction_WP3.md)
            - [BB_Template_filled_ServiceMesh_WP3](/library/unsorted_BB/Daniel/BB_Template_filled_ServiceMesh_WP3.md)
    - In-Vehicle
        - [BB-EST](/library/In-Vehicle/BB-EST/BB-EST.md)
        - [BB-SC-TC](/library/In-Vehicle/BB-SC-TC/BB-SC-TC.md)
            - Testing
                - [BB_Shadowing](/library/In-Vehicle/BB-SC-TC/Testing/BB_Shadowing.md)
                - [BB_Digital_Twin](/library/In-Vehicle/BB-SC-TC/Testing/BB_Digital_Twin.md)
            - [hsfhjgkhfjd](/library/In-Vehicle/BB-MU/hsfhjgkhfjd.md)
        - [BB-SC](/library/In-Vehicle/BB-SC/BB-SC.md)
            - [MWLayer](/library/In-Vehicle/BB-SC/MWLayer/MWLayer.md)
                - Time
                    - [BB_Time_Service](/library/In-Vehicle/BB-SC/MWLayer/Time/BB_Time_Service.md)
                - Configuration
                    - [BB_OTA_Master](/library/In-Vehicle/BB-SC/MWLayer/Configuration/BB_OTA_Master.md)
                    - [BB_Local_Update_Manager](/library/In-Vehicle/BB-SC/MWLayer/Configuration/BB_Local_Update_Manager.md)
                - Storage
                    - [BB_Vehicle_Data_Collector](/library/In-Vehicle/BB-SC/MWLayer/Storage/BB_Vehicle_Data_Collector.md)
                    - [BB_Vehicle_Logging_and_Recording](/library/In-Vehicle/BB-SC/MWLayer/Storage/BB_Vehicle_Logging_and_Recording.md)
                    - [BB_Vehicle_Data_Persistency](/library/In-Vehicle/BB-SC/MWLayer/Storage/BB_Vehicle_Data_Persistency.md)
                - Security
                    - [BB_Security_Event_Manager](/library/In-Vehicle/BB-SC/MWLayer/Security/BB_Security_Event_Manager.md)
                    - [BB_Secure_Onboard_Communication](/library/In-Vehicle/BB-SC/MWLayer/Security/BB_Secure_Onboard_Communication.md)
                    - [BB_Crypto_Service_Manager](/library/In-Vehicle/BB-SC/MWLayer/Security/BB_Crypto_Service_Manager.md)
                    - [BB_Security_Transport_Layer](/library/In-Vehicle/BB-SC/MWLayer/Security/BB_Security_Transport_Layer.md)
                    - [BB_Internet_Protocol_Security](/library/In-Vehicle/BB-SC/MWLayer/Security/BB_Internet_Protocol_Security.md)
                    - [BB_Intrusion_Detection](/library/In-Vehicle/BB-SC/MWLayer/Security/BB_Intrusion_Detection.md)
                - Communication
                    - [BB_Communication_Service_S2S](/library/In-Vehicle/BB-SC/MWLayer/Communication/BB_Communication_Service_S2S.md)
                    - [BB_Gateway_Mirroring](/library/In-Vehicle/BB-SC/MWLayer/Communication/BB_Gateway_Mirroring.md)
                    - [BB_Network_Management](/library/In-Vehicle/BB-SC/MWLayer/Communication/BB_Network_Management.md)
                    - [BB_Standard_Android_VHAL](/library/In-Vehicle/BB-SC/MWLayer/Communication/BB_Standard_Android_VHAL.md)
                    - [BB_SecOS](/library/In-Vehicle/BB-SC/MWLayer/Communication/BB_SecOS.md)
                    - [BB_Smart_Charging_Communication](/library/In-Vehicle/BB-SC/MWLayer/Communication/BB_Smart_Charging_Communication.md)
                - Runtime
                    - [BB_State_Management](/library/In-Vehicle/BB-SC/MWLayer/Runtime/BB_State_Management.md)
                    - [BB_Diagnostic_Services_Applications](/library/In-Vehicle/BB-SC/MWLayer/Runtime/BB_Diagnostic_Services_Applications.md)
                - Power-Management
                    - [BB_Power_Management](/library/In-Vehicle/BB-SC/MWLayer/Power-Management/BB_Power_Management.md)
                - Diagnostics
                    - [BB_Diagnostic_Policy_Manager](/library/In-Vehicle/BB-SC/MWLayer/Diagnostics/BB_Diagnostic_Policy_Manager.md)
                - Tools-and-Methods
                    - [BB_Key_Management_System](/library/In-Vehicle/BB-SC/MWLayer/Tools-and-Methods/BB_Key_Management_System.md)
                - Platform-Health-Management
                    - [BB_Distributed_Health_Management](/library/In-Vehicle/BB-SC/MWLayer/Platform-Health-Management/BB_Distributed_Health_Management.md)
                    - [BB_Watchdog](/library/In-Vehicle/BB-SC/MWLayer/Platform-Health-Management/BB_Watchdog.md)
            - [AppLayer](/library/In-Vehicle/BB-SC/AppLayer/AppLayer.md)
                - Communication
                    - [BB_AOSP_Push_Notification_Service](/library/In-Vehicle/BB-SC/AppLayer/Communication/BB_AOSP_Push_Notification_Service.md)
            - HWLayer
            - [OSLayer](/library/In-Vehicle/BB-SC/OSLayer/OSLayer.md)
                - Time
                    - [BB_Automotive_Edge_Runtime](/library/In-Vehicle/BB-SC/OSLayer/Time/BB_Automotive_Edge_Runtime.md)
    - [S-BB](/library/S-BB/S-BB.md)
        - MWLayer
            - [BB_Standardized_way_for_Reasoning_on_Data_Streams](/library/S-BB/MWLayer/BB_Standardized_way_for_Reasoning_on_Data_Streams.md)
            - [BB_Standardized_Data_Description_for_Vehicle_Sensors_Attributes_Actuators](/library/S-BB/MWLayer/BB_Standardized_Data_Description_for_Vehicle_Sensors_Attributes_Actuators.md)
            - [BB_SOA](/library/S-BB/MWLayer/BB_SOA.md)
        - [MWLayer](/library/S-BB/MWLayer/MWLayer.md)
            - [BB_Standardized_Data_Conversion_Tools_for_Info_Knowledge_Layers](/library/S-BB/MWLayer/BB_Standardized_Data_Conversion_Tools_for_Info_Knowledge_Layers.md)
            - [BB_sSOA](/library/S-BB/MWLayer/BB_sSOA.md)
        - [AppLayer](/library/S-BB/AppLayer/AppLayer.md)
            - [BB_Standardized_Architectural_Patterns_for_Cross_Platform_Data_Service_Infrastructure](/library/S-BB/AppLayer/BB_Standardized_Architectural_Patterns_for_Cross_Platform_Data_Service_Infrastructure.md)
            - [BB_Standardization_of_Vehicle_API](/library/S-BB/AppLayer/BB_Standardization_of_Vehicle_API.md)
            - [BB_Standardized_Description_of_Data_from_Related_Domains](/library/S-BB/AppLayer/BB_Standardized_Description_of_Data_from_Related_Domains.md)
            - [BB_Standardized_Procedure_and_Tooling_for_Modelling_Data_from_Different_Domains](/library/S-BB/AppLayer/BB_Standardized_Procedure_and_Tooling_for_Modelling_Data_from_Different_Domains.md)
            - [BB_Standardized_Procedure_and_Tooling_for_Combining_Data_from_Different_Domains](/library/S-BB/AppLayer/BB_Standardized_Procedure_and_Tooling_for_Combining_Data_from_Different_Domains.md)
        - HWLayer
        - OSLayer
    - Cloud
        - [BB-CSC-TC](/library/Cloud/BB-CSC-TC/BB-CSC-TC.md)
        - [BB-CSC](/library/Cloud/BB-CSC/BB-CSC.md)
        - BB-CMU
        - [BB-CEST](/library/Cloud/BB-CEST/BB-CEST.md)
            - _Not_Clustered
                - [BB_Car_Simulator](/library/Cloud/BB-CEST/_Not_Clustered/BB_Car_Simulator.md)
***
generated using [README Generator](/scripts/readme_generator.py)