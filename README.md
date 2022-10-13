# BordereauxAUTOMATION
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


