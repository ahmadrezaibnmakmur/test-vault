# OKR Automate- Disbursement - Extraction Notes

Source: /Users/ahmadreza/Downloads/OKR Automate- Disbursement.pptx
Slides: 52
Media files: 36
Native chart objects: 0
Native table objects: 5

## Slide 1
### Text
- Google Shape;55;p13: OKRAutomate- Disbursement
- Google Shape;56;p13: 2025 - Rahman Aribowo
### Pictures
- Google Shape;54;p13 -> ppt/media/image2.png

## Slide 2
### Text
- Google Shape;62;p14: Define Phase
### Pictures
- Google Shape;61;p14 -> ppt/media/image2.png

## Slide 3
### Text
- Google Shape;67;p15: Background
- Google Shape;68;p15: The disbursement process is still semi-automated, meaning transfers can only be made at the earliest on H+1 from the transaction date, typically in the afternoon. On Mondays, this can extend into the evening.Manual checking by the finance team is required before transfers, so disbursements can only be processed on business days.Data reconciliation is necessary due to various transaction data issues, which impact lead time.
- Google Shape;69;p15: DEFINE PHASE

## Slide 4
### Text
- Google Shape;74;p16: As Is Process Map
- Google Shape;75;p16: DEFINE PHASE
- Google Shape;76;p16: Process SummaryThe system initiates the disbursement process.System calculates transaction details automatically.AP Staff compiles transaction data for processing.AP Staff reviews and reconciles the compiled data.Data Analyst adjusts data if discrepancies are found.AP Staff processes the fund transfer after reconciliation.The disbursement process is completed.
- Google Shape;77;p16: Overall Process
### Pictures
- Google Shape;78;p16 -> ppt/media/image7.jpg

## Slide 5
### Text
- Google Shape;83;p17: As Is Process Map
- Google Shape;84;p17: DEFINE PHASE
- Google Shape;85;p17: Process SummaryAP Staff downloads transaction reports from the system one by one.AP Staff re-formats the reports using an Excel macro for standardization.
- Google Shape;86;p17: Compiling Data
### Pictures
- Google Shape;87;p17 -> ppt/media/image11.jpg

## Slide 6
### Text
- Google Shape;92;p18: As Is Process Map
- Google Shape;93;p18: DEFINE PHASE
- Google Shape;94;p18: Process SummaryAP Staff checks the applicable rate.AP Staff verifies transaction details.AP Staff checks bank account information.AP Staff reviews for discrepancies across all checks.AP Staff lists the discrepancies in an Excel file.AP Staff informs the Data Analyst of the issue.Data Analyst investigates and adjusts the data as needed.Process is completed after adjustments.
- Google Shape;95;p18: Reconciling Data
### Pictures
- Google Shape;96;p18 -> ppt/media/image3.jpg

## Slide 7
### Text
- Google Shape;101;p19: As Is Process Map
- Google Shape;102;p19: DEFINE PHASE
- Google Shape;103;p19: Process SummaryThe Data Analyst categorizes the issue into one of four types.Technical - Fix the issue in the engine and rerun the engine process.Contract - Fix or update the contract in CMS and update the fixing status.Bank Account - Update bank account data and fixing status.Transaction - Clarify the transaction issue with the merchant.End the process.
- Google Shape;104;p19: Adjusting Data
### Pictures
- Google Shape;105;p19 -> ppt/media/image13.jpg

## Slide 8
### Text
- Google Shape;110;p20: As Is Process Map
- Google Shape;111;p20: DEFINE PHASE
- Google Shape;112;p20: Process SummaryAP Staff reviews the adjusted data.Transactions are pushed in bulk to Xendit.Finance Supervisor reviews the transaction data in Xendit.Finance Supervisor decides whether to approve.System executes the fund transfer.AP Staff sends a notification email (linked from point A).The disbursement process is completed.
- Google Shape;113;p20: Transferring Fund
### Pictures
- Google Shape;114;p20 -> ppt/media/image9.jpg

## Slide 9
### Text
- Google Shape;120;p21: Measure Phase
### Pictures
- Google Shape;119;p21 -> ppt/media/image2.png

## Slide 10
### Text
- Google Shape;125;p22: Disburse Time by Month - 2024
- Google Shape;126;p22: MEASURE PHASE
- Google Shape;130;p22: The increase in monthly transactions is influenced by the addition of new clients and the number of disbursement days.The rise in disbursement volume does not affect process stability.
### Pictures
- Google Shape;127;p22 -> ppt/media/image5.png
- Google Shape;128;p22 -> ppt/media/image6.png
- Google Shape;129;p22 -> ppt/media/image34.png

## Slide 11
### Text
- Google Shape;135;p23: Overall Disburse Time - 2024
- Google Shape;136;p23: MEASURE PHASE
- Google Shape;138;p23: The majority of disbursements occur between 3 PM (15:00) and 5 PM (17:00).The peak frequency is at 4 PM (16:00), indicating this is the most common hour for disbursements.There is a noticeable drop after 6 PM, with very few disbursements beyond 8 PM (20:00).Disbursements before 1 PM (13:00) are rare, suggesting most processes happen in the afternoon.The distribution is right-skewed, which means while most disbursements are clustered in the mid-afternoon, a few occur late in the day.
### Pictures
- Google Shape;137;p23 -> ppt/media/image12.png
- Google Shape;139;p23 -> ppt/media/image8.png

## Slide 12
### Text
- Google Shape;145;p24: Error Rate - 2024
- Google Shape;146;p24: MEASURE PHASE
- Google Shape;150;p24: We implemented a ticketing system to track issues in July 2024.The error rate is calculated as the number of transactions that contain at least one error.
### Pictures
- Google Shape;147;p24 -> ppt/media/image14.png
- Google Shape;148;p24 -> ppt/media/image20.png

## Slide 13
### Text
- Google Shape;155;p25: Metrics
- Google Shape;156;p25: MEASURE PHASE
- Google Shape;158;p25: We measure disbursement time and the percentage of adjustments that affect it. Additionally, we analyze the impact of national holidays on disbursement delays, as these delays can influence customer satisfaction.
### Native Tables
Table 1:
| No | Metric | UoM | Baseline | Target |
| 1 | Disburse Lead Time Average | Time in hrs | 16.2 | 12 |
| 2 | Error Rate (Jul - Dec 2024) | Percent | 3.4% | 0.5% |
| 3 | Disburse Delayed Due to Holiday (Q1-Q3 2024) | Days | 13 | 0 |

## Slide 14
### Text
- Google Shape;164;p26: Analyze Phase
### Pictures
- Google Shape;163;p26 -> ppt/media/image2.png

## Slide 15
### Text
- Google Shape;169;p27: Pareto Chart - Disburse Lead Time
- Google Shape;170;p27: Apart from the above processes, the calculation process in DWH takes longer, especially on Mondays.
- Google Shape;171;p27: ANALYZE PHASE
### Pictures
- Google Shape;172;p27 -> ppt/media/image10.png

## Slide 16
### Text
- Google Shape;177;p28: Disbursement Lead Time Issue
- Google Shape;178;p28: ANALYZE PHASE
- Google Shape;179;p28: Why-why Analysis
- Google Shape;180;p28: 1.	Data Calculation Takes 6 hours on AverageLimitation on calculation engine capabilities 2.	Data Compiling Takes 1.5 hours on AverageThere's no bulk file download featuresReport templates do not yet follow the standard set by the Finance Team

## Slide 17
### Text
- Google Shape;185;p29: Disbursement Lead Time Issues
- Google Shape;186;p29: ANALYZE PHASE
- Google Shape;187;p29: Why-why Analysis
- Google Shape;188;p29: 3.	Reconcile Process Takes 3 Hours in AverageManual reconciliation is still required due to a high error rateFinance team manually compares transactions processed through the ESBPay payment gateway with those processed through non-ESBPay using disbursement data and the PG dashboardErrors persist because of recurring issues, even though they’ve already been reportedTechnical issues (will be detailed on 14th page) 4.	Data Adjustment Process Takes 90 Minutes on AverageAdjustment is done by the Data Team in the systemOnly the Data Team has access to modify the system dataThere’s no adjustment features for Finance Team

## Slide 18
### Text
- Google Shape;193;p30: Disbursement Lead Time Issues
- Google Shape;194;p30: ANALYZE PHASE
- Google Shape;195;p30: Why-why Analysis
- Google Shape;196;p30: 5. 	Manual Email Drafting Takes 90 Minutes on AverageData adjustments are only made at the summary level, not at the transaction detail level No feature available to auto-send emails Report templates do not yet follow the standard set by the Finance Team

## Slide 19
### Text
- Google Shape;202;p31: ANALYZE PHASE
- Google Shape;204;p31: Pareto Chart - Technical Issues Breakdown
### Pictures
- Google Shape;203;p31 -> ppt/media/image15.png

## Slide 20
### Text
- Google Shape;209;p32: Disbursement Technical Issue
- Google Shape;210;p32: ANALYZE PHASE
- Google Shape;211;p32: Why-why Analysis
- Google Shape;212;p32: 1.	Rounding DiscrepanciesDifferent formulas are used by the engine and the finance teamThe engine deducts delivery cost directly, while Finance uses (rounded delivery fee + rounded delivery VAT)Rounding logic differs for cash transactions  Rounding logic differs for platform fee transactions 2.	Max Cap Calculation per Outlet is IncorrectThe engine does not yet support max cap calculation per outlet

## Slide 21
### Text
- Google Shape;217;p33: Disbursement Technical Issue
- Google Shape;218;p33: ANALYZE PHASE
- Google Shape;219;p33: Why-why Analysis
- Google Shape;220;p33: 3.	Manual Push Required – Client Requests Morning TransferCurrent flow: Finance must reconcile first, then push transactions in bulk to XenditNo feature to disburse transactions individually for special cases4.	Discount Does Not Match ContractPrice and discount are not created in the system for manual contractsNo SOP to review and update master data after manual contract creationNo PIC assigned to update the first ESO date, leading to incorrect discount calculations for MDR ESBThere is a discrepancy between the price list and discount stated in the contract and the formula set in the CMSDiscount details in the disbursement report show as zeroA bug in the disbursement engine causes discount details to not appear in transactions

## Slide 22
### Text
- Google Shape;225;p34: Disbursement Technical Issue
- Google Shape;226;p34: ANALYZE PHASE
- Google Shape;227;p34: Why-why Analysis
- Google Shape;228;p34: 5.	MDR ESO Rate Does Not Match ContractMDR ESO rate in the system does not match the contract and master price listNo SOP to review and update master data after manual contract creationEditing access for pricelist and contracts is still open to multiple user roles. Human errors occurred during the editing process6.	Double Disbursement DataA contract renewal occurred and the system did not automatically map the company code to the new contractData was incorrectly joined to branch code instead of company code from legality, causing potential duplication in the disbursement master.

## Slide 23
### Text
- Google Shape;233;p35: Disbursement Technical Issue
- Google Shape;234;p35: ANALYZE PHASE
- Google Shape;235;p35: Why-why Analysis
- Google Shape;236;p35: 7.	Incorrect Disbursement AmountWrong formula used for cash transactionsCorrect formula should be: -(MDR ESB - MDR ESB Discount - Delivery Fee - VAT Delivery)8.	MDR ESB is still being counted for clients with “Auto-debit” : “No”.System error in reading Auto-debit flagging.

## Slide 24
### Text
- Google Shape;241;p36: Disbursement Technical Issue
- Google Shape;242;p36: ANALYZE PHASE
- Google Shape;243;p36: Why-why Analysis
- Google Shape;244;p36: 9.	Refunded Transactions Still Included in Disbursement DataThe system cannot detect transactions that have already been refunded by ESBRefund done manually and no feature to input refund.10.	Client Complained – Transaction Not DisbursedCustomer balance was deducted, but transaction status remained unsettled.Transactions were already settled in POS and PG, but their status in the Online Fund report was still marked as Pending.Callbacks from the Ipay team were delayed by 2–3 days.Client Performed ESO Transactions Without PG RegistrationNo SOP in place to ensure PG registration during the client onboarding process.

## Slide 25
### Text
- Google Shape;249;p37: Disbursement Technical Issue
- Google Shape;250;p37: ANALYZE PHASE
- Google Shape;251;p37: Why-why Analysis
- Google Shape;252;p37: 12.	Incorrect Delivery Cost DeductionESO delivery order failed to get a courier and was delivered by the outlet manuallyNo system flag or indicator to mark orders that failed to get a courier and were delivered by the outlet.13.	Disbursement billing shows a negative value.The value of online transactions is not sufficient to cover the MDR from cash transactions.14.	Non-PG ESB Client Transactions Included in Disbursement DataPG ESB client settings are configured manually by the Operations team.

## Slide 26
### Text
- Google Shape;257;p38: Disbursement Technical Issue
- Google Shape;258;p38: ANALYZE PHASE
- Google Shape;259;p38: Why-why Analysis
- Google Shape;260;p38: 15.	Client Bank Account Information is IncorrectNo SOP in place for bank account validation Multiple sources need to be updated whenever there's a bank account changeSLA for payment gateway data changes has not been defined16.	Other IssueThe disbursement process is still dependent on data checking by the finance team and data fixing by the data teamSome clients request disbursement transfers on the 27th and 28th of each month

## Slide 27
### Text
- Google Shape;265;p39: Issue Recap
- Google Shape;266;p39: ANALYZE PHASE
### Pictures
- Google Shape;267;p39 -> ppt/media/image33.png

## Slide 28
### Text
- Google Shape;272;p40: Issue Recap
- Google Shape;273;p40: ANALYZE PHASE
### Pictures
- Google Shape;274;p40 -> ppt/media/image36.png

## Slide 29
### Text
- Google Shape;279;p41: Issue Recap
- Google Shape;280;p41: ANALYZE PHASE
### Pictures
- Google Shape;281;p41 -> ppt/media/image35.png

## Slide 30
### Text
- Google Shape;286;p42: Waste & Variance: Operational & Lead Time
- Google Shape;287;p42: ANALYZE PHASE
### Native Tables
Table 1:
| Variance | Waste |
| Metode pengambilan dan kompilasi data untuk rekonsiliasi | Download manual per file report untuk rekonsiliasi |
| Standarisasi report daily disbursement | Update manual delivery cost pada report daily disbursement |
| Metode rekonsiliasi transaksi | Manual rekonsiliasi menggunakan excel (cash in) dan macro (detail & summary disbursement) |
| Pencatatan diskon dan max cap | Finance mencatat manual diskon & max cap pada excel setiap harinya setelah disbursement |

## Slide 31
### Text
- Google Shape;293;p43: Waste & Variance: Operational & Lead Time
- Google Shape;294;p43: ANALYZE PHASE
### Native Tables
Table 1:
| Variance | Waste |
| Metode pengiriman report daily disbursement | Manual drafting & send email report daily disbursement kepada client |
| Metode validasi nomor rekening client | Manual validasi melalui m-banking/online payment |
|  | Double check data rekap nomor rekening client oleh finance pada gsheet admin |

## Slide 32
### Text
- Google Shape;301;p44: Improve Phase
### Pictures
- Google Shape;300;p44 -> ppt/media/image2.png

## Slide 33
### Text
- Google Shape;306;p45: Possible Solution
- Google Shape;307;p45: ANALYZE PHASE
### Pictures
- Google Shape;308;p45 -> ppt/media/image19.png

## Slide 34
### Text
- Google Shape;313;p46: Possible Solution
- Google Shape;315;p46: ANALYZE PHASE
### Pictures
- Google Shape;316;p46 -> ppt/media/image25.png

## Slide 35
### Text
- Google Shape;321;p47: Possible Solution
- Google Shape;323;p47: ANALYZE PHASE
### Pictures
- Google Shape;324;p47 -> ppt/media/image28.png

## Slide 36
### Text
- Google Shape;329;p48: Implementation Plan
- Google Shape;330;p48: IMPROVE PHASE
### Native Tables
Table 1:
| No | Project | Status | PIC | Due Date |
| 1 | Price, Disc & ESO Scheme Setting Standard for Special Case Contract | Completed | Rahman | 9/11/2024 |
| 2 | Disbursement Report Bulk Download | Completed | Rahman | 9/17/2024 |
| 3 | Disbursement Report Table Formatting | Completed | Rahman | 9/17/2024 |
| 4 | Limit User Role Access to Price & Discount | Completed | Rahman | 10/30/2024 |
| 5 | Enhancement Contract Mapping - CMS | Completed | Ale | 12/10/2024 |
| 6 | Limit Bank Account Change Request to H+1 | Completed | Nabila | 1/31/2025 |
| 7 | Cleaning Data & SOP Master Disbursement | Completed | Rahman | 2/3/2025 |
| 8 | PG Request Data Validation Flow | Completed | Nabila | 2/3/2025 |
| 9 | Adjustment Feature [New Engine] | In Progress | Rahman | 5/1/2025 |
| 10 | Auto Email Feature [New Engine] | In Progress | Rahman | 5/1/2025 |
| 11 | Update Disbursement Push Manual Status [New Engine] | In Progress | Rahman | 5/13/2025 |
| 12 | Schedule & QRIS Transaction Setting Enhancement [New Engine] | In Progress | Rahman | 5/16/2025 |
| 13 | PG Registration for DB Migration | In Progress | Rahman | 5/30/2025 |
| 14 | Negative Disbursement Value Management | In Progress | Rahman | 5/31/2025 |
| 15 | Streamline Pending Transaction Issue Handling in CMS | In Progress | Rahman | 6/30/2025 |
| 16 | Disbursement Calculations Revamp | In Progress | Rahman | 7/10/2025 |
| 17 | PG Tagging by Transaction | In Progress | Rahman |  |
| 18 | Streamline Refund Transaction Issue Handling in CMS | In Progress | Rahman |  |
| 19 | Streamline Delivery Cost Issue Handling in CMS | In Progress | Rahman |  |
| 20 | Auto-fill First ESO Date [New Engine] | In Progress | Rahman |  |
| 21 | PG Dashboard vs Disbursement Data Reconciliation | In Progress | Rahman |  |
| 22 | Enable Auto Transfer Flow [New Engine] | In Progress | Rahman |  |

## Slide 37
### Text
- Google Shape;336;p49: Picture of Improvement
- Google Shape;337;p49: IMPROVE PHASE
- Google Shape;339;p49: Price, Disc & ESO Scheme Setting Standard for Special Case Contract
- Google Shape;341;p49: Set discount after issue
- Google Shape;342;p49: Set discount when creating a discount template
- Google Shape;352;p49: Before
- Google Shape;374;p49: After
### Pictures
- Google Shape;338;p49 -> ppt/media/image16.png
- Google Shape;340;p49 -> ppt/media/image17.png

## Slide 38
### Text
- Google Shape;379;p50: Picture of Improvement
- Google Shape;380;p50: IMPROVE PHASE
- Google Shape;383;p50: Data Compiling Takes 1.5 hours on Average
- Google Shape;384;p50: Data Compiling only takes < 10 mins
- Google Shape;395;p50: Before
- Google Shape;417;p50: After
### Native Tables
Table 1:
| Disbursement Report Bulk Download |
| Disbursement Report Table Formatting |
### Pictures
- Google Shape;381;p50 -> ppt/media/image32.png
- Google Shape;382;p50 -> ppt/media/image23.jpg

## Slide 39
### Text
- Google Shape;422;p51: Picture of Improvement
- Google Shape;424;p51: IMPROVE PHASE
- Google Shape;425;p51: Limit User Role Access to Price & Discount
- Google Shape;436;p51: Before
- Google Shape;458;p51: After
- Google Shape;459;p51: Potential accidental edit on price list and discount by Finance Team.
### Pictures
- Google Shape;423;p51 -> ppt/media/image27.png
- Google Shape;426;p51 -> ppt/media/image26.png

## Slide 40
### Text
- Google Shape;465;p52: Picture of Improvement
- Google Shape;467;p52: IMPROVE PHASE
- Google Shape;468;p52: Enhancement Contract Mapping - CMS
- Google Shape;469;p52: Lack of control over renewal contracts caused duplicate disbursement data
- Google Shape;470;p52: Auto-rename comcode after the contract is approved
- Google Shape;483;p52: Before
- Google Shape;505;p52: After
### Pictures
- Google Shape;464;p52 -> ppt/media/image24.png
- Google Shape;471;p52 -> ppt/media/image29.png
- Google Shape;472;p52 -> ppt/media/image18.png

## Slide 41
### Text
- Google Shape;510;p53: Picture of Improvement
- Google Shape;512;p53: IMPROVE PHASE
- Google Shape;513;p53: Same day bank account change leads to manual adjustment
- Google Shape;514;p53: Limit Bank Account Change Request to H+1
- Google Shape;524;p53: Before
- Google Shape;546;p53: After
### Pictures
- Google Shape;547;p53 -> ppt/media/image21.png

## Slide 42
### Text
- Google Shape;552;p54: Picture of Improvement
- Google Shape;554;p54: IMPROVE PHASE
- Google Shape;555;p54: Cleaning Data & SOP Master Disbursement
- Google Shape;565;p54: Before
- Google Shape;587;p54: After
- Google Shape;589;p54: Difference MDR rate and discount between contract and the formula in CMS
### Pictures
- Google Shape;588;p54 -> ppt/media/image22.png

## Slide 43
### Text
- Google Shape;594;p55: Picture of Improvement
- Google Shape;596;p55: IMPROVE PHASE
- Google Shape;597;p55: Before
- Google Shape;598;p55: After
- Google Shape;607;p55: OK!
- Google Shape;609;p55: -
- Google Shape;610;p55: PG Request Data Validation Flow

## Slide 44
### Text
- Google Shape;615;p56: To-Be Process Map
- Google Shape;617;p56: IMPROVE PHASE

## Slide 45
### Text
- Google Shape;622;p57: Data Analysis: Before vs After
- Google Shape;624;p57: IMPROVE PHASE

## Slide 46
### Text
- Google Shape;629;p58: Cost/Benefit Analysis
- Google Shape;631;p58: IMPROVE PHASE

## Slide 47
### Text
- Google Shape;637;p59: Control Phase
### Pictures
- Google Shape;636;p59 -> ppt/media/image2.png

## Slide 48
### Text
- Google Shape;642;p60: Process Control Plan
- Google Shape;644;p60: CONTROL PHASE

## Slide 49
### Text
- Google Shape;649;p61: Control Chart
- Google Shape;651;p61: CONTROL PHASE

## Slide 50
### Text
- Google Shape;656;p62: Benefit of The Project
- Google Shape;658;p62: CONTROL PHASE

## Slide 51
### Text
- Google Shape;663;p63: Project Closing Documentation
- Google Shape;665;p63: CONTROL PHASE
### Pictures
- Google Shape;666;p63 -> ppt/media/image30.png

## Slide 52
- No extracted text/picture/chart objects found.
