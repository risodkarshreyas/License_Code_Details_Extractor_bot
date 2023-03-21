** For next run ensure logic to capture and save license status is added to License_Code_Details_Extractor_bot before executing**

1) Run Boon_LicenseExtractorBot
2) Output stored in License_details.xlsx file
3) Apply filter - Bundle = UiPath Platform / Server AND Subscription = (HAPOELA or Enterprise or HAPOELA-NonProd) AND END Date > Current  Date
4) Open solution License_Code_Details_Extractor_bot and from data folder , rename + Archive the License_details_Input.xlsx and License_details_Output.xlsx files
5) Clear the contents of License_details_Input.xlsx and License_details_Output.xlsx files
6) Paste the filtered output of License_details.xlsx into License_details_Input.xlsx file sheet named Orchestrator_Overview
7) Within License_details_Input.xlsx file  Copy License code and URL columns from Orchestrator_Overview sheet and psate in Orchestrator_Details sheet
8) Run License_Code_Details_Extractor_bot bot and captured output is stored in License_details_Output.xlsx (See if status can be captured - Run keywise status extractor workflow sequence)
9) Apply filter  for Prod & Non prod and paste in the report to be shared with customer Orchestrator tab after filtering out disabled keys


In the main report :
a) Clear current content of dealhub report sheet, add latest LO content
b) Apply Filter - bundlename = Attended Robot Named User and product name = Attended Robot Named User.remove any trial or disabled licenses
c) Apply Filter - bundlename = Studio Named User and product name = Studio Named User, remove any trial or disabled licenses
d) Apply Filter - SubscriptionName= Citizen Dev - HAPOELAX and product name = StudioX Named User, remove any trial or disabled licenses