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

# getsafe 
1. Missing values are highlighted for:
a. vertical
b. product
c. claim type and others
2. Incident event at should be before Date of notification. If there is an error you can find at what zendesk no. the error is present in this column "the claim at which the Incident event is> DON".
3. Claims payout should be less than issued sum.
4.Checked for duplicates for claims no. and if there are any duplicates the column we need to check is "Duplicates_inClaimsno".
5. checking for whether policy end date is after policy start date. To check if error are present, the column is ""PolicyStartend_falseinfo(claims number"

# Helvetia claims(TPA)
1. Schadenbetrag bezahlt (SB bereits abgezogen) = TPA Rechnungbetrag - Selbstbehalt
2. Status should all be übernommen.
3. checked for zendesk duplicates if present then check the column "duplcate_zendesk_list"
4. Checked for if there are any error present in riskoende-risikostart, Vertragsende gem. Zertifikat/voraussichtliches Vertragsende-Vertragsbeginn gem. Zertifikat. The results you may find it in "DifferenceRisk", "Differencevertrag" respectively.

# Trias claims
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

# GAVAG claims
1. 1. Duplicate check for Zendesk no. has been done and the results are stored in the "Duplicate_zendesk_in table". 
2. Missing values are highlighted for:
a. Sitz des händler
b. fallart
c. schaden anmeldung and other schaden
3. Schaden anmeldung date should be always greater than schadendatum.

# Helvetia claims(RS_B)
1. Duplicate check for Zendesk no. has been done and the results are stored in the "Duplicate_zendesk_in table". 
2. Missing values are highlighted for:
a. Sitz des händler
b. vertags typ
c.schaden protokol
d. TPA and others.
3. Checking if there are error in dates of following columns
a. Risikostart and risiko end
b. Vertragsbeginn gem. Zertifikat and Vertragsende gem. Zertifikat/voraussichtliches Vertragsende

