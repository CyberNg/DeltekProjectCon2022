For people newer to Visual Studio and T-SQL, I created three versions of the RDL. All three versions have identical Main Tables, but build up in complexity:

1) ProjectCon_2022_NO_CustomOptions_or_Grouping.rdl
ReportVersion: ProjectCon_V1
Base SQL with only Extended Where Clause.

2) ProjectCon_2022_NO_CustomOptions.rdl
ReportVersion: ProjectCon_V2
Same as Number 1, but includes Extended Grouping.

3) ProjectCon_2022_Final.rdl
ReportVersion: ProjectCon_V3
This is the final report shown during the session, with all the bell and whistles (Custom Options, Parameters, and Grouping) included.
Note: this will need Custom Options added to the front-tier as shown in the ProjectCon 2022 Session (ProjectCon_Vantagepoint_2022_Session_VP-55.pptx).

The RDL’s were developed using the VantagepointDemo, with at least the 202106 Accounting Period.

To run the Report Dataset T-SQL scripts in SSMS include the Declarations, for example:
DECLARE @ActiveCompany nVARCHAR( 10 ) = '01'
DECLARE @ActivePeriod INT = 202106
