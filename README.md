# US federal and state holidays — open data

Every US federal holiday (2025–2028) and, for **all 50 states**, the paid holidays of **state government employees** (2026–2028): which federal holidays state offices observe, which extra days they close, floating days, local and partial days — each state checked against its **official source**.

Maintained by [the-calendar.net](https://the-calendar.net/) · License: [CC BY 4.0](LICENSE.md) · Last verified: 2026-10-14

## Why this exists

"State holidays" lists on the web usually mix legal observances, county-only days and commemorations with actual days off. This dataset answers a narrower, practical question: **on which days are a state's own offices closed?** That is what payroll, scheduling, court and permit deadlines depend on.

## Files

| File | What |
|---|---|
| [`data/federal/us-federal-holidays.csv`](data/federal/us-federal-holidays.csv) | 11 federal holidays per year, date and observed date (5 U.S.C. § 6103) |
| `data/federal/<year>.json` | same, one file per year |
| [`data/states/state-holidays-2026-2028.csv`](data/states/state-holidays-2026-2028.csv) | one row per state × year × holiday; `type` federal/state, `state_offices_closed` yes/no |
| `data/states/<state>.json` | full profile per state: source, weekend rule, renamed federal days, extra holidays, floating days, local/partial days, election days |
| [`data/rankings/state-paid-holidays-2027.csv`](data/rankings/state-paid-holidays-2027.csv) | states ranked by paid holidays in 2027 (range 9–14) — see the [interactive map](https://the-calendar.net/holidays/by-state/most-paid-holidays/) |
| `datapackage.json` | [Frictionless Data](https://frictionlessdata.io/) descriptor |

### Live versions (always current)

- JSON API: `https://the-calendar.net/api/holidays/by-state/<state>/<year>.json` — [endpoint index](https://the-calendar.net/api/index.json)
- Calendar subscriptions (iCalendar, updates itself in Google/Apple/Outlook): `https://the-calendar.net/downloads/states/<state>-holidays.ics`, federal: `https://the-calendar.net/downloads/us-federal-holidays.ics`
- Per-state pages with printable PDFs: [https://the-calendar.net/holidays/by-state/](https://the-calendar.net/holidays/by-state/)

## Definitions

- **Paid holidays** (ranking metric) = federal holidays on which state offices close + additional full, statewide paid state holidays.
- A federal holiday renamed by a state (e.g. "Lincoln/Washington Day" on Presidents' Day) counts once and is listed under `renamedFederalHolidays`.
- **Not counted:** floating/personal days (`floatingDays`), half-days and county-/city-only days (`partialOrLocal`), election days that are holidays only in election years (`electionDay`).
- **Confederate-era holidays** are excluded from calendars and the ranking by editorial policy; where they still close state offices they are documented under `excludedConfederateHolidays`.
- Weekend rule: when a holiday falls on a weekend, most states observe it on the adjacent Friday or Monday (`weekendRule` per state). Dates in the data are the calendar dates; federal rows also carry `observed_date`.
- Collective bargaining agreements can give specific bargaining units different days; the data reflects each state's general schedule.

## Sources

- **Alabama**: [HB165 (2025 RS, enrolled; amends Ala. Code 1-3-8, adds Juneteenth, effective 2025-06-01) + Alabama State Personnel Board Rule 670-X-12-.01 (Holidays) + RSA 2026 state holiday list (rsa-al.gov/about-rsa/holidays/)](https://alison.legislature.state.al.us/files/pdf/SearchableInstruments/2025RS/HB165-enr.pdf) (2026)
- **Alaska**: [2027 State Calendar - State Holidays (Alaska Division of Finance, revised 09/29/2025); cross-checked with 2026 Holiday Schedule (doa.alaska.gov/dof/payroll/resource/hldy2026.pdf, by bargaining unit) and AS 44.12.010](https://doa.alaska.gov/dof/payroll/resource/calendar2027.pdf) (2027)
- **Arizona**: [ADOA Human Resources '2027 Holiday Calendar' and '2026 Holiday Calendar' (hr.az.gov); Ariz. Admin. Code R2-5A-B601 (Holidays); A.R.S. 1-301](https://hr.az.gov/2027-holiday-calendar) (2027)
- **Arkansas**: [Arkansas DSAS Office of Personnel Management Policy 52, 'Holidays and Birthday Leave' (eff. 2025-05-22), authority Ark. Code 1-5-101 to -104; Arkansas Secretary of State '2026 State Holidays' list (sos.arkansas.gov/uploads/holidays_2026.pdf)](https://sas.arkansas.gov/wp-content/uploads/52-Holidays-and-Birthday-Leave-5.23.2025.pdf) (2026)
- **California**: [CalHR 'State Holidays' (2026 Holiday Dates; references Gov. Code 19853, 19853.2, 19854)](https://www.calhr.ca.gov/about-calhr/divisions-programs/personnel-management/leave-benefits/state-holidays/) (2026)
- **Colorado**: [Colorado Dept. of Revenue 'Colorado State Holidays' (2026 State Holiday Schedule) + C.R.S. 24-11-101 (Legal holidays) + C.R.S. 24-11-112; DHR 'Calendar Year 2026 State of Colorado Holiday Schedule'](https://tax.colorado.gov/holidays) (2026)
- **Connecticut**: [Connecticut DAS 'Observance of 2027 Connecticut State Holidays' (C.G.S. 1-4); also DAS 2026 holiday list (portal.ct.gov/das/services-for-state-employees/holidays)](https://portal.ct.gov/das/-/media/das/statewide-hr/a---z-listing-task-pdfs/holidays---state-employee-observance-of-holidays---2027.pdf?rev=ee236f575c454ee1859e71e2d20b3423) (2027)
- **Delaware**: [Delaware Department of Human Resources '2027 State Holidays' and '2026 State Holidays' (1 Del. C. ch. 501, 501(a))](https://dhr.delaware.gov/holidays/2027.shtml) (2027)
- **Florida**: [Florida Statutes s. 110.117 'Paid holidays' (2026 online edition); s. 683.01 'Legal holidays'](http://www.leg.state.fl.us/statutes/index.cfm?App_mode=Display_Statute&URL=0100-0199/0110/Sections/0110.117.html) (2026)
- **Georgia**: [Team Georgia 'State of Georgia Holiday Schedule' (2026 and 2027, per Gov. Kemp's annual holiday memo); georgia.gov 'Georgia State Holidays 2026'; DOAS state holiday events](https://team.georgia.gov/all-articles/state-georgia-holiday-schedule) (2027)
- **Hawaii**: [State of Hawai'i - Holidays to be observed in 2026 and 2027 (Dept. of Human Resources Development, created 01/12/2026; cites HRS 8-1)](https://dhrd.hawaii.gov/wp-content/uploads/2026/06/State-Holidays-2026-2027.pdf) (2027)
- **Idaho**: [Idaho Division of Human Resources, Executive Branch Statewide Policy Section 20: Holiday Leave (est. 06/2026), plus idaho.gov State Holidays table (2026) and Idaho Code 73-108](https://dhr.idaho.gov/wp-content/uploads/2026/07/DHR-20_Holiday.pdf) (2026)
- **Illinois**: [Illinois Dept. of Central Management Services - State Holidays / memorandum 'State Holiday Calendar for 2026 and 2027' (Nov 18, 2025); 80 Ill. Adm. Code 303.190](https://cms.illinois.gov/personnel/employeeresources/stateholidays.html) (2027)
- **Indiana**: [Indiana Office of the Governor memorandum 'List of the 2027 state holidays' (via State Personnel Department state holidays page and Holidays Policy, eff. Aug 14, 2023)](https://secure.in.gov/spd/benefits/files/2027%20Holidays%20Memorandum.pdf) (2027)
- **Iowa**: [Iowa DAS Centralized Payroll - State Holidays 2026 (posted 12/29/25) and Iowa Code 2026 section 1C.2 'Paid holidays'](https://das.iowa.gov/state-employees/state-accounting/centralized-payroll/state-holidays) (2026)
- **Kansas**: [Kansas Dept. of Administration, Office of Personnel Services - Holidays for 2026 (State of Kansas Executive Branch); K.A.R. 1-9-2](https://admin.ks.gov/offices/personnel-services/agency-information/holidays-for-state-of-kansas-executive-branch-employees/holidays-for-2026) (2026)
- **Kentucky**: [Kentucky Personnel Cabinet - Holidays and Leave: State Holidays (2026 list); KRS 18A.190, KRS 2.190; Personnel Memo 24-20](https://extranet.personnel.ky.gov/Pages/Leave.aspx) (2026)
- **Louisiana**: [Louisiana State Civil Service - Job Aid 'Understanding State Holidays' (La. R.S. 1:55) with General Circulars 2025-051, 2025-053, 2026-010, 2026-023 and Governor's proclamations 71 and 74 JML 2025, 06 and 07 JML 2026](https://civilservice.louisiana.gov/files/HRHandbook/JobAid/11-Understanding%20State%20Holidays.pdf) (2026)
- **Maine**: [Maine Bureau of Human Resources, HR Memorandum 2-25 '2026 and 2027 Holiday Schedules for State Agency Employees Not Covered by a Collective Bargaining Agreement' (Sept 4, 2025); BHR Policy Manual - Holidays](https://www.maine.gov/bhr/sites/bhr/files/inline-files/HR%20Memo%202-25%20_0.pdf) (2027)
- **Maryland**: [Maryland Dept. of Budget and Management - State Holidays for the Year 2026; Maryland Manual 'State Employee Holidays' (msa.maryland.gov); Md. Code, State Personnel and Pensions 9-201](https://dbm.maryland.gov/employees/Pages/StateHolidays2026.aspx) (2026)
- **Massachusetts**: [Absence and Leave Policies (Holiday Leave) - Mass.gov / HRD; HRD memo 'Legal Holidays at the Commonwealth of Massachusetts' dated Dec 30, 2024 (calendar years 2025 and 2026); 2027 dates cross-checked against MA DESE 'Massachusetts Legal Holiday Calendar 2026, 2027, 2028, 2029' (Sep 10, 2026)](https://www.mass.gov/guides/absence-and-leave-policies) (2026)
- **Michigan**: [State Holidays - State of Michigan (per Civil Service Commission Regulation 5.08)](https://www.michigan.gov/som/government/state-holidays) (2026)
- **Minnesota**: [2027 MSGC Regular Meeting Calendar - 'State of Minnesota Executive Branch Holidays 2027' (Minnesota Sentencing Guidelines Commission, dated 5/14/2026)](https://mn.gov/sentencing-guidelines/assets/8-2027MSGCMeetingCalendar_tcm30-767110.pdf) (2027)
- **Mississippi**: [FY 2027 Mississippi State Employee Handbook, ch. 3.1 Holidays (MSPB, effective 7/1/2026); Miss. Code Ann. 3-3-7 (Secretary of State 'State Holidays' page); Governor's holiday proclamations 2026](https://www.mspb.ms.gov/employee-resources/state-employee-handbook) (2026)
- **Missouri**: [State Holidays - Missouri Office of Administration (2026 list)](https://oa.mo.gov/commissioner/state-holidays) (2026)
- **Montana**: [Holiday Policy - Montana State Human Resources Division (last reviewed June 5, 2026); MCA 1-1-216, 2-18-601(9), 2-18-603 (Montana Code Annotated 2025)](https://charitablegiving.mt.gov/_docs/shrd/Policies/Holiday_Policy.pdf) (2026)
- **Nebraska**: [A. Holidays - Nebraska Judicial Branch personnel rules (follows Neb. Rev. Stat. 25-2221); cross-checked with Nebraska Accountability and Disclosure Commission / Dept. of Transportation office-closure schedules and University of Nebraska holiday list](https://nebraskajudicial.gov/holidays) (2026)
- **Nevada**: [NRS 236.015 Legal holidays (as amended by AB 140, 2023); State of Nevada 'State Holidays' schedule and FY2026 payroll holiday schedule (hr.nv.gov)](https://www.leg.state.nv.us/nrs/nrs-236.html) (2026)
- **New Hampshire**: [State Holiday Schedule - NH Employee Portal (NH Division of Personnel / DAS); links printable calendars for 2026 and 2027](https://www.employeeportal.nh.gov/compensation-savings/state-holiday-schedule) (2027)
- **New Jersey**: [State Holidays - NJ.gov (holidays observed by State agencies in 2026; also 2025); NJ Dept. of Health HR benefits sheet '13 paid holidays' (updated 7/9/2024)](https://www.nj.gov/nj/about/facts/holidays.shtml) (2026)
- **New Mexico**: [State of New Mexico Paid Holiday Schedule for 2026 (State Personnel Board, General Memorandum 2025-015, 12 Dec 2025)](https://www.spo.state.nm.us/wp-content/uploads/2026-Paid-Holiday-Schedule-1.pdf) (2026)
- **New York**: [2027 Calendar of Legal Holidays for State Employees in the Classified Service of the Executive Branch (NYS Department of Civil Service); with Attendance and Leave Manual Advisory Memorandum 2026-04](https://www.cs.ny.gov/attendance_leave/2027_legal_holidays.cfm) (2027)
- **North Carolina**: [2027 Holiday Schedule (NC Office of State Human Resources); also https://oshr.nc.gov/state-employee-resources/benefits/leave/holidays](https://oshr.nc.gov/documents/2027-holiday-schedule/open) (2027)
- **North Dakota**: [N.D. Cent. Code ch. 1-03 Holidays (sections 1-03-01, 1-03-01.1, 1-03-02, 1-03-02.1); NDAC 4-07-07-06; OMB 'Being part of Team ND: benefits and extras' (10 paid holidays)](https://ndlegis.gov/cencode/t01c03.pdf) (2026)
- **Ohio**: [Ohio Revised Code 124.19 State holidays (eff. Sept 30, 2021; read via Wayback snapshot of Oct 2025); LSC Members Brief 'State Holidays' (Mar 2022)](https://codes.ohio.gov/ohio-revised-code/section-124.19) (2026)
- **Oklahoma**: [Official State Holidays 2027 (OMES; Governor's Executive Order 2026-26 under 25 O.S. 82.1); 2026 per Executive Order 2025-14](https://oklahoma.gov/omes/divisions/human-capital-management/employee-benefits/leave-holidays/holidays.html) (2027)
- **Oregon**: [2026 Holiday memo for unrepresented employees (DAS Chief Human Resources Office, 11 Dec 2025; State HR Policy 60.010.01); SEIU Local 503/State of Oregon CBA 2025-2027 Article 58](https://www.oregon.gov/das/HR/Documents/2026%20Holiday%20Memo.pdf) (2026)
- **Pennsylvania**: [Administrative Circular 26-14 - Holidays - 2027 (PA Office of Administration, 6 Oct 2026; Executive Board resolution BD-26-001)](https://www.pa.gov/content/dam/copapwp-pagov/en/oa/documents/policies/ac/26-14.pdf) (2027)
- **Rhode Island**: [2027 Payroll & Holiday Calendar, 'State Holiday Celebrations' (RI Department of Administration, Division of Human Resources; hosted on courts.ri.gov); R.I. Gen. Laws 25-1-1; Council 94 master agreement Art. 9 (2013-2017)](https://www.courts.ri.gov/Public-Resources/Documents/StateHolidays2.pdf) (2027)
- **South Carolina**: [Holiday Leave - 2026 and 2027 Holiday Schedule (SC Department of Administration, State Human Resources; read via Wayback snapshot of 4 Sep 2026); S.C. Code 53-5-10 and 53-5-30](https://admin.sc.gov/services/state-human-resources/benefits-and-leave/holiday-leave) (2027)
- **South Dakota**: [South Dakota State Employee Handbook (6/24/2026), Holidays section; SDCL 1-5-1 (https://sdlegislature.gov/Statutes/1-5-1)](https://bhraonline.sd.gov/handbook.pdf) (2026)
- **Tennessee**: [State Holidays - About Tennessee (TN.gov) 2026 closure list; HR Support 'What are TN State Government holidays?'; State of Tennessee Attendance & Leave Manual ch. 7 (https://www.tn.gov/content/dam/tn/hr/documents/ALManual.pdf)](https://www.tn.gov/about-tn/state-holidays.html) (2026)
- **Texas**: [State Holiday Schedule for Fiscal Year 2027 (Texas State Auditor's Office); also Comptroller 'State of Texas Holiday Schedule, Fiscal Year 2027' https://comptroller.texas.gov/about/holidays.php; Tex. Gov't Code ch. 662](https://hr.sao.texas.gov/Documents/Holidays/Holidays2027.pdf) (2027)
- **Utah**: [Utah Code 63G-1-301 Legal holidays - Personal preference day (version effective 1/1/2027); State of Utah 2026 Schedule of Pay Periods and Holidays (https://finance.utah.gov/wp-content/uploads/2026PP.pdf)](https://le.utah.gov/xcode/Title63G/Chapter1/C63G-1-S301_2026050620270101.pdf) (2027)
- **Vermont**: [State of Vermont Holiday Schedule - Effective July 1, 2026 - June 30, 2028 (Vermont Department of Human Resources; PDF https://humanresources.vermont.gov/sites/humanresources/files/documents/State%20of%20Vermont%20Holiday%20Schedule.pdf); 1 V.S.A. 371](https://humanresources.vermont.gov/benefits-wellness/holiday-schedule) (2027)
- **Virginia**: [2027 Pay and Holiday Calendar (Virginia Department of Human Resource Management, published Sept 2026); Va. Code 2.2-3300 (https://law.lis.virginia.gov/vacode/title2.2/chapter33/section2.2-3300/)](https://www.dhrm.virginia.gov/docs/default-source/default-document-library/2027-pay-and-holiday-calendar.pdf?sfvrsn=19dff6ab_2) (2027)
- **Washington**: [State holiday schedule 2026-2027 (WA Department of Revenue); OFM 'Vacation, leave and holidays' https://ofm.wa.gov/state-human-resources/compensation-job-classes/compensation-administration/vacation-leave-and-holidays; RCW 1.16.050; WAC 357-31-005](https://dor.wa.gov/contact/state-holiday-schedule) (2027)
- **West Virginia**: [Holidays - Paid Leave Information and Forms (WV Division of Personnel); W. Va. Code 2-2-1 (https://code.wvlegislature.gov/2-2-1/)](https://personnel.wv.gov/employee-resources/paid-leave-information-and-forms) (2026)
- **Wisconsin**: [Leave Benefits and State Holidays (Wisconsin Division of Personnel Management; https://dpm.wi.gov/Pages/How_Do_I/seeStateHolidays.aspx); Wisconsin Human Resources Handbook ch. 716 (https://dpm.wi.gov/Hand%20Book%20Chapters/WHRH_Ch_716.pdf); Wis. Stat. 230.35(4)](https://dpm.wi.gov/Pages/Employees/BnLeave.aspx) (2026)
- **Wyoming**: [State Holidays and Office Closures (Wyoming Administration & Information); 006-6 Wyo. Code R. 6-4 Holiday Leave; W.S. 8-4-101](https://ai.wyo.gov/about-us/state-holidays-and-office-closures) (2026)

Found an error or a change for next year? [Open an issue](../../issues) with a link to the official source.

## Attribution

CC BY 4.0. Please credit with a link, for example:

```html
Holiday data: <a href="https://the-calendar.net/">the-calendar.net</a> (CC BY 4.0)
```

## How it is built

The data is generated from the source of [the-calendar.net](https://the-calendar.net/), where every federal date is computed from 5 U.S.C. § 6103 and every state holiday is stored as a date rule (e.g. "fourth Friday of November") verified against the state's official schedule. Releases are tagged by verification date.
