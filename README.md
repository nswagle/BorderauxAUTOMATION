# BordereauxAUTOMATION(CLAIMS)
In this Bordereaux auomation. we have claims prüflogik for the following risk carriers
A. LV1871 claims
B. Helvetia RS(B)
C. Helvetia TPA(B)
D. Trias claims
E. GAVAG claims
F. Getsafe claims


# A. LV1871 claims
1. Duplicate check for Zendesk no. has been done and the results are stored in the "Duplicate_zendesk_in table". 
2. Missing values are highlighted for:
a. Vertragsbeginn gem. Zertifikat
b. Vertragsende gem. Zertifikat/voraussichtliches Vertragsende
c. Schadentyp aus Schadenmeldung
d. Schadentyp aus Schadenprotokoll
e. Datum Schadenfall bezahlt
3. Checking if there are error in dates of following columns
a. Risikostart and risiko end
b. Vertragsbeginn gem. Zertifikat and Vertragsende gem. Zertifikat/voraussichtliches Vertragsende
c. checking for schadendatum is before schadenanmeldung.
4. 	Versicherungssumme is greater than schadenbetrag bezahlt

Duplicate_zendesk_in table: This column will list down the duplicates zendesk no. which are present 
Diff_risk_end_start_Error(zendesk): This column will list down if there are any errors in risikostart and risikoend
Diff_vertrag_end_start_Error(zendesk): This column will list down if there are any errors in Vertragsbeginn gem. Zertifikat and Vertragsende gem. Zertifikat/voraussichtliches Vertragsende

# B. getsafe 
1. Missing values are highlighted for:
a. vertical
b. product
c. claim type and others
2. Incident event at should be before Date of notification. If there is an error you can find at what zendesk no. the error is present in this column "the claim at which the Incident event is> DON".
3. Claims payout should be less than issued sum.
4.Checked for duplicates for claims no. and if there are any duplicates the column we need to check is "Duplicates_inClaimsno".
5. checking for whether policy end date is after policy start date. To check if error are present, the column is ""PolicyStartend_falseinfo(claims number"

# C. Helvetia claims(TPA)
1. Schadenbetrag bezahlt (SB bereits abgezogen) = TPA Rechnungbetrag - Selbstbehalt
2. Status should all be übernommen.
3. checked for zendesk duplicates if present then check the column "duplcate_zendesk_list"
4. Checked for if there are any error present in riskoende-risikostart, Vertragsende gem. Zertifikat/voraussichtliches Vertragsende-Vertragsbeginn gem. Zertifikat. The results you may find it in "DifferenceRisk", "Differencevertrag" respectively.

# D. Trias claims
1. Duplicate check for Zendesk no. has been done and the results are stored in the "Duplicate_zendesk_in table". 
2. Missing values are highlighted for:
a. Vertragsbeginn gem. Zertifikat
b. Vertragsende gem. Zertifikat/voraussichtliches Vertragsende
c. Schadentyp aus Schadenmeldung
d. Schadentyp aus Schadenprotokoll
e. Datum Schadenfall bezahlt
3. Checking if there are error in dates of following columns
a. Risikostart and risiko end
b. Vertragsbeginn gem. Zertifikat and Vertragsende gem. Zertifikat/voraussichtliches Vertragsende
c. checking for schadendatum is before schadenanmeldung.
4. 	Versicherungssumme is greater than schadenbetrag bezahlt

Duplicate_zendesk_in table: This column will list down the duplicates zendesk no. which are present 
Diff_risk_end_start_Error(zendesk): This column will list down if there are any errors in risikostart and risikoend
Diff_vertrag_end_start_Error(zendesk): This column will list down if there are any errors in Vertragsbeginn gem. Zertifikat and Vertragsende gem. Zertifikat/voraussichtliches Vertragsende.

# E. GAVAG claims
1. 1. Duplicate check for Zendesk no. has been done and the results are stored in the "Duplicate_zendesk_in table". 
2. Missing values are highlighted for:
a. Sitz des händler
b. fallart
c. schaden anmeldung and other schaden
3. Schaden anmeldung date should be always greater than schadendatum.

# F. Helvetia claims(RS_B)
1. Duplicate check for Zendesk no. has been done and the results are stored in the "Duplicate_zendesk_in table". 
2. Missing values are highlighted for:
a. Sitz des händler
b. vertags typ
c.schaden protokol
d. TPA and others.
3. Checking if there are error in dates of following columns
a. Risikostart and risiko end
b. Vertragsbeginn gem. Zertifikat and Vertragsende gem. Zertifikat/voraussichtliches Vertragsende


# BordereauxAUTOMATION(Sales)
In this Bordereaux auomation. we have sales prüflogik for the following risk carriers
A. Getsafe sales
B. Helvetia Risikofortfall
C. Helvetia Sales
D. Trias sales
E. GAVAG sales
F. LV1871 sales

# A.Getsafe sales
1. Duplicate check for Customer contract no. has been done and the results are stored in the "Duplicates_in_Customer Contract Number".
2. Underwriting date should be less than policy start date. If not then their zendesk no. are listed in the column "Underwriting_>_policy_start_date(Customer Contract Number)"
3. Highlighting missing values: vertical, product group, product getsafe, product partner, market, isurance object detail.
4. Policy end date should be later than policy start date. if not then check the difference of the dates in "DifferencePolicy(In days)". If there are any negative dates mentioned then we have an error.
5. For every policy runtime we have we have a specific value
Policy Runtime-         premium interval
1 Month-                    P1M
1 Year-                     P1Y
24months-                   P1I

# B. HELVETIA Risikofortfall
1.Risikonettobeitrag(New) should be equal to multiplication of Verkaufpreis and  Risikonettobeitrag(old)
2.Risikobruttobeitrag(New) should be equal to multiplication of Verkaufpreis and  Risikobruttobeitrag(old)
3.Versicherungsteuer(New)  should be equal to multiplication of Verkaufpreis and  Versicherungsteuer(old)
4.Duplicate check for Zertifikat no. has been done and the results are stored in the "Duplicates_inZeertifikatnummer"
5.Vertragsende should be after vertrags beginn if not then the error can be identified out by difference of them stored in "VDifferenceRisk"
6.Risikoende should be after risikostart if not then the error can be identified out by difference of them stored in "RDifferenceRisk"
7.In fallart the data should be risikofortfall or beitragsrückerstattung. If it is something else as schaden auszahlung then convert it to  risikofortfall or beitragsrückerstattung based on Verwendungszweck	R,B
8.Highlighting the missing values in Sitzdes handler and other columns.

# C. Helvetia sales
1. Duplicate check for Zertifikat no. has been done and the results are stored in the "Duplicates_inZeertifikatnummer"
2. Highlighting the missing values in product bezeichnung and other columns.
3. Vertragsende should be after vertrags beginn if not then the error can be identified out by difference of them stored in "VDifferenceRisk"
4. Risikoende should be after risikostart if not then the error can be identified out by difference of them stored in "RDifferenceRisk"
5. For merging the data of helvetia sales and helvetia risikofortfall, Please check mergingsheets.py file.

# D. Trias sales
1. Zertikat no. and Periode auf Bestellebene values are grouped in "groupingby.xlsx".
2. Buchung datum should be less than equal to period beginn. if not then their zendesk no. are present here "Buchungdatum which are > period_beginn(Zertifikat NO.)"
3. Note:Wichtig!! For every außerordentliche Kündigung zum we should have Kündigungsgrund. This data will be present in output code but not onto finalform trias. If the count of both are same then no worries and if not then manually it can be checked.
4. Periodende should be after Periodstart if not then the error can be identified out by difference of them stored in "Differenceperiod_biginn_end" if negative dates difference present then we have an error
5. Highlighting the missing values in Qualitat, insurance basis and others.

# E. Gavag Sales
1. Duplicate check for Zertifikat no. has been done and the results are stored in the "Duplicates_inZeertifikatnummer"
2. Highlighting the missing values in product bezeichnung and other columns.
3. Kaufdatum should be less than vertragsbeginn and if not then then their zertifikat no. are listed down in "kaufdatum greater than vertragsbeginn(Zertifikat no. for those)" column.
4. Vertragsende should be after vertrags beginn if not then the error can be identified out by difference of them stored in "VDifferenceRisk"
5. Risikoende should be after risikostart if not then the error can be identified out by difference of them stored in "RDifferenceRisk"
6. ende der versicherung should be after Beginn der... if not then the error can be identified out by difference of them stored in "RDifferenceRisk"
# F. LV1871 sales
1. Zertikat no. and Periode auf Bestellebene values are grouped in "groupingby.xlsx".
2. Buchung datum should be less than equal to period beginn. if not then their zendesk no. are present here "Buchungdatum which are > period_beginn(Zertifikat NO.)"
3. Note:Wichtig!! For every außerordentliche Kündigung zum we should have Kündigungsgrund. This data will be present in output code but not onto finalform trias. If the count of both are same then no worries and if not then manually it can be checked.
4. Periodende should be after Periodstart if not then the error can be identified out by difference of them stored in "Differenceperiod_biginn_end" if negative dates difference present then we have an error
5. Highlighting the missing values in Qualitat, insurance basis and others.
