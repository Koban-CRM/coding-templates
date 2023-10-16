# Modèle de document Devis

Voici le code correspondant  à la déclaration des champs d'un modèle de document Devis.

**Version Compatible** : Juin 2021 et supérieures

```xml
<DataSets>
    <DataSet Name="client">
      <Fields>
        <Field Name="NOM">
          <DataField>NOM</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADR_COMPLEMENT">
          <DataField>ADR_COMPLEMENT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADR_NOVOIE">
          <DataField>ADR_NOVOIE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADR_RUE">
          <DataField>ADR_RUE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADR_VILLE">
          <DataField>ADR_VILLE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADR_CPOSTAL">
          <DataField>ADR_CPOSTAL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PHONE">
          <DataField>PHONE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="FAX">
          <DataField>FAX</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="EMAIL">
          <DataField>EMAIL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="SIRET">
          <DataField>SIRET</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRFAC_COMPLEMENT">
          <DataField>ADRFAC_COMPLEMENT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRFAC_RUE">
          <DataField>ADRFAC_RUE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRFAC_VILLE">
          <DataField>ADRFAC_VILLE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRFAC_CP">
          <DataField>ADRFAC_CP</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ACCOUNTINGCODE">
          <DataField>ACCOUNTINGCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="EXTCODE">
          <DataField>EXTCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ISTTC">
          <DataField>ISTTC</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NOTVA">
          <DataField>NOTVA</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADR_COUNTRY">
          <DataField>ADR_COUNTRY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="THIRDLOGO">
          <DataField>THIRDLOGO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="FIRSTNAME">
          <DataField>FIRSTNAME</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="GENDER">
          <DataField>GENDER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="MOBILE">
          <DataField>MOBILE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="OTHERCODE">
          <DataField>OTHERCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="opportunite">
      <Fields>
        <Field Name="LIBELLE">
          <DataField>LIBELLE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DESCRIPTION">
          <DataField>DESCRIPTION</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TELAFFECTE">
          <DataField>TELAFFECTE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="EMAILAFFECTE">
          <DataField>EMAILAFFECTE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NOMAFFECTE">
          <DataField>NOMAFFECTE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="MOBILEAFFECTE">
          <DataField>MOBILEAFFECTE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="opportspecfield">
      <Fields>
        <Field Name="SPECFIELD1">
          <DataField>SPECFIELD1</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="SPECFIELD2">
          <DataField>SPECFIELD2</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="SPECFIELD3">
          <DataField>SPECFIELD3</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="SPECFIELD4">
          <DataField>SPECFIELD4</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="SPECFIELD5">
          <DataField>SPECFIELD5</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="SPECFIELD6">
          <DataField>SPECFIELD6</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="SPECACCOUNTFIELD1">
          <DataField>SPECACCOUNTFIELD1</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="SPECACCOUNTFIELD2">
          <DataField>SPECACCOUNTFIELD2</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="devis">
      <Fields>
        <Field Name="DATEENVOI">
          <DataField>DATEENVOI</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
   <Field Name="DATECREATION">
          <DataField>DATECREATION</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="NUMERO">
          <DataField>NUMERO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="LIBELLE">
          <DataField>LIBELLE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PIEDPAGE">
          <DataField>PIEDPAGE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="LOGO">
          <DataField>LOGO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TELPAR">
          <DataField>TELPAR</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="EMAILPAR">
          <DataField>EMAILPAR</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PAR">
          <DataField>PAR</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>

        <Field Name="NOMCONTACT">
          <DataField>NOMCONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DATELIVRAISON">
          <DataField>DATELIVRAISON</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="DUREETRAVAUX">
          <DataField>DUREETRAVAUX</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="BACKCOLOR">
          <DataField>BACKCOLOR</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PERIODEVALIDITE">
          <DataField>PERIODEVALIDITE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="MODERGLT">
          <DataField>MODERGLT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NOMSOCIETE">
          <DataField>NOMSOCIETE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="FORMECAPITAL">
          <DataField>FORMECAPITAL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRESSE1">
          <DataField>ADRESSE1</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRESSE2">
          <DataField>ADRESSE2</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="SIREN">
          <DataField>SIREN</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="RCS">
          <DataField>RCS</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="APE">
          <DataField>APE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NOTVA">
          <DataField>NOTVA</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="MENTIONCOMPL">
          <DataField>MENTIONCOMPL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="FAXCONTACT">
          <DataField>FAXCONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="MAILCONTACT">
          <DataField>MAILCONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PHONECONTACT">
          <DataField>PHONECONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="HEADER">
          <DataField>HEADER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="FOOTER">
          <DataField>FOOTER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="FONCTIONCONTACT">
          <DataField>FONCTIONCONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CURRENCYSYMBOL">
          <DataField>CURRENCYSYMBOL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DELIVCOMPL">
          <DataField>DELIVCOMPL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DELIVRUE">
          <DataField>DELIVRUE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DELIVVILLE">
          <DataField>DELIVVILLE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DELIVCP">
          <DataField>DELIVCP</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DELIVCOUNTRY">
          <DataField>DELIVCOUNTRY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DELIVNAMECONTACT">
          <DataField>DELIVNAMECONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DELIVFIRSTNAMECONTACT">
          <DataField>DELIVFIRSTNAMECONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DELIVPHONE">
          <DataField>DELIVPHONE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ECHEANCE">
          <DataField>ECHEANCE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CPTFAC_NOM">
          <DataField>CPTFAC_NOM</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CPTFAC_ADRS">
          <DataField>CPTFAC_ADRS</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CUSTOMERREFERENCE">
          <DataField>CUSTOMERREFERENCE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TRACKINGURL">
          <DataField>TRACKINGURL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="RIB">
          <DataField>RIB</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="IBAN">
          <DataField>IBAN</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="BIC">
          <DataField>BIC</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="MOBILECONTACT">
          <DataField>MOBILECONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="MOBILEPAR">
          <DataField>MOBILEPAR</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="lignes">
      <Fields>
        <Field Name="SECTIONID">
          <DataField>SECTIONID</DataField>
          <rd:TypeName>System.Int32</rd:TypeName>
        </Field>
        <Field Name="LIBELLE">
          <DataField>LIBELLE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="COMMENTAIRE_SECTION">
          <DataField>COMMENTAIRE_SECTION</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DESIGNATION">
          <DataField>DESIGNATION</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="COMMENTAIRE">
          <DataField>COMMENTAIRE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="UNITE">
          <DataField>UNITE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PRIXUNITAIRE">
          <DataField>PRIXUNITAIRE</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="HT">
          <DataField>HT</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="QUANTITE">
          <DataField>QUANTITE</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="REDUCTION">
          <DataField>REDUCTION</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="TTC">
          <DataField>TTC</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="TVA">
          <DataField>TVA</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="REFERENCE">
          <DataField>REFERENCE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PRDSF1">
          <DataField>PRDSF1</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PRDSF2">
          <DataField>PRDSF2</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="HTTPS">
          <DataField>HTTPS</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="BARCODE">
          <DataField>BARCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ISCTR">
          <DataField>ISCTR</DataField>
          <rd:TypeName>System.Boolean</rd:TypeName>
        </Field>
        <Field Name="HT_PUCTR">
          <DataField>HT_PUCTR</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="TTC_PUCTR">
          <DataField>TTC_PUCTR</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="HT_NOCTR">
          <DataField>HT_NOCTR</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="TTC_NOCTR">
          <DataField>TTC_NOCTR</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="PRIXPAR">
          <DataField>PRIXPAR</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="CATPRODUCT_LABEL">
          <DataField>CATPRODUCT_LABEL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CLASSIF">
          <DataField>CLASSIF</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TVA5">
          <DataField>TVA5</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="TVA10">
          <DataField>TVA10</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="TVA20">
          <DataField>TVA20</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="PRODUCTLOGO">
          <DataField>PRODUCTLOGO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="REDUCTION_CTR">
          <DataField>REDUCTION_CTR</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="PACKING">
          <DataField>PACKING</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CF1">
          <DataField>CF1</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CF2">
          <DataField>CF2</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="detailtva">
      <Fields>
        <Field Name="TAUX">
          <DataField>TAUX</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="HT">
          <DataField>HT</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="TVA">
          <DataField>TVA</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
  </DataSets>
```

## Définition des champs

| Nom DataSet     | Nom Champ          | Définition                             |
| --------------- | ------------------ | -------------------------------------- |
| client          | NOM                | Nom du client                          |
| client          | ADR_COMPLEMENT     | Adresse / Complément client            |
| client          | ADR_NOVOIE         | Non utilisé                            |
| client          | ADR_RUE            | Adresse / Rue client                   |
| client          | ADR_VILLE          | Adresse / Ville client                 |
| client          | ADR_CPOSTAL        | Adresse / Code Postal client           |
| client          | ADR_COUNTRY        | Adresse / Pays client                  |
| client          | PHONE              | Téléphone client                       |
| client          | FAX                | N° de fax client                       |
| client          | EMAIL              | Email client                           |
| client          | SIRET              | N° de siret client                     |
| client          | ADRFAC_COMPLEMENT  | Adresse de facturation / Complément    |
| client          | ADRFAC_RUE         | Adresse de facturation / Rue           |
| client          | ADRFAC_VILLE       | Adresse de facturation / Ville         |
| client          | ADRFAC_CP          | Adresse de facturation / Code postal   |
| client          | ADRFAC_COUNTRY     | Adresse de facturation / Pays          |
| client          | ACCOUNTINGCODE     | Compte comptable client                |
| client          | EXTCODE            | Code externe client                    |
| client          | ISTTC              |                                        |
| client          | NOTVA              | N° TVA client                          |
| Opportunité     | LIBELLE            | Libellé opportunité                    |
| Opportunité     | DESCRIPTION        | Commenrtaire opportunité               |
| Opportunité     | TELAFFECTE         | Téléphone personne affectée            |
| Opportunité     | EMAILAFFECTE       | EMail personne affectée                |
| Opportunité     | NOMAFFECTE         | Personne affectée                      |
| devis           | DATEENVOI          | Date d'envoi                           |
| devis           | DATECREATION       | Date de création du devis              |
| devis           | NUMERO             | N° de devis                            |
| devis           | LIBELLE            | Libellé devis                          |
| devis           | PIEDPAGE           | Texte Pied de page                     |
| devis           | LOGO               | Logo structure                         |
| devis           | TELPAR             | Téléphone personne affectée            |
| devis           | EMAILPAR           | EMail personne affectée                |
| devis           | PAR                | Nom et prénom personne affectée        |
| devis           | NOMCONTACT         | Nom contact client                     |
| devis           | DATELIVRAISON      | Date de livraion devis                 |
| devis           | DUREETRAVAUX       | Durée des travaux devis                |
| devis           | BACKCOLOR          | Couleur de fond du modèle de document  |
| devis           | PERIODEVALIDITE    | Période de validité                    |
| devis           | MODERGLT           | Mode de règlement                      |
| devis           | NOMSOCIETE         | Nom Structure                          |
| devis           | FORMECAPITAL       | Forme Capital Structure                |
| devis           | ADRESSE1           | Adresse 1 Structure                    |
| devis           | ADRESSE2           | Adresse 2 Structure                    |
| devis           | SIREN              | SIREN Structure                        |
| devis           | RCS                | Non utilisé                            |
| devis           | APE                | Non utilisé                            |
| devis           | NOTVA              | Numéro TVA Structure                   |
| opportspecfield | SPECFIELD1         | Non utilisé                            |
| opportspecfield | SPECFIELD2         | Non utilisé                            |
| opportspecfield | SPECFIELD3         | Non utilisé                            |
| opportspecfield | SPECFIELD4         | Non utilisé                            |
| opportspecfield | SPECFIELD5         | Non utilisé                            |
| opportspecfield | SPECFIELD6         | Non utilisé                            |
| opportspecfield | SPECACCOUNTFIEL1   | Non utilisé                            |
| opportspecfield | SPECACCOUNTFIEL2   | Non utilisé                            |
| devis           | DATEENVOI          | Date d'envoi                           |
| devis           | NUMERO             | Numéro devis                           |
| devis           | LIBELLE            | Libellé devis                          |
| devis           | PIEDPAGE           | Pied de page                           |
| devis           | LOGO               | Logo                                   |
| devis           | TELPAR             | Téléphone personne affectée            |
| devis           | EMAILPAR           | EMail personne affectée                |
| devis           | PAR                | Personne affectée                      |
| devis           | NOMCONTACT         | Nom contact client                     |
| devis           | DATELIVRAISON      | Date de livraison devis                |
| devis           | DUREETRAVAUX       | Durée des travaux                      |
| devis           | BACKCOLOR          | Couleur de fond du modèle de document  |
| devis           | PERIODEVALIDITE    | Période de validité                    |
| devis           | MODERGLT           | Mode de règlement                      |
| devis           | NOMSOCIETE         | Nom Structure                          |
| devis           | FORMECAPITAL       | Forme Capital Structure                |
| devis           | ADRESSE1           | Adresse 1 Structure                    |
| devis           | ADRESSE2           | Adresse 2 Structure                    |
| devis           | SIREN              | SIREN Structure                        |
| devis           | RCS                | Non utilisé                            |
| devis           | APE                | Non utilisé                            |
| devis           | NOTVA              | Numéro TVA Structure                   |
| devis           | MENTIONCOMPL       | Mentions complémentaire Structure      |
| devis           | FAXCONTACT         | N° de fax contact client               |
| devis           | MAILCONTACT        | Email contact client                   |
| devis           | PHONECONTACT       | Télephone contact client               |
| devis           | FONCTIONCONTACT    | Fonction contact client                |
| devis           | HEADER             | Texte Entête                           |
| devis           | FOOTER             | Texte Pied de page                     |
| devis           | CURRENCYSYMBOL     | Devise                                 |
| devis           | DELIVCOMPL         | Adresse Livraison / Complément Client  |
| devis           | DELIVRUE           | Adresse Livraison / Rue Client         |
| devis           | DELIVVILLE         | Adresse Livraison / Ville Client       |
| devis           | DELIVCP            | Adresse Livraison / Code Postal Client |
| devis           | ECHEANCE           | Échéance                               |
| devis           | CPTFAC_NOM         | Nom/Libellé compte de facturation      |
| devis           | CPT_FACADRS        | Adresse compte de facturation          |
| devis           | CUSTOMERREFERENCE  | Référence client                       |
| devis           | TRACKINGURL        | Non utilisé                            |
| devis           | RIB                | RIB Structure                          |
| devis           | IBAN               | IBAN Structure                         |
| devis           | BIC                | BIC Structure                          |
| devis           | MOBILECONTACT      | N° de mobile du contact client         |
| devis           | MOBILEPAR          | Mobile personne affectée               |
| lignes          | SECTIONID          | Identifiant Section                    |
| lignes          | LIBELLE            | Libellé Section                        |
| lignes          | COMMENTAIRESECTION | Commentaire section                    |
| lignes          | DESIGNATION        | Libellé ligne                          |
| lignes          | COMMENTAIRE        | Commentaire ligne                      |
| lignes          | UNITE              | Unité                                  |
| lignes          | PRIXUNITAIRE       | Prix unitaire                          |
| lignes          | HT                 | Montant HT                             |
| lignes          | QUANTITE           | Quantité                               |
| lignes          | REDUCTION          | Réduction                              |
| lignes          | TTC                | Montant TTC                            |
| lignes          | TVA                | Montant TVA                            |
| lignes          | REFERENCE          | Référence Produit interne              |
| lignes          | PRDSF1             |                                        |
| lignes          | PRDSF2             |                                        |
| lignes          | HTTPS              | URL eBoutique                          |
| lignes          | BARCODE            | Code barre                             |
| lignes          | ISCTR              | Est un produit avec tarif client       |
| lignes          | HT_PUCTR           | Montant HT prix tarif client           |
| lignes          | TTC_PUCTR          | Montant TTC prix tarif client          |
| lignes          | HT_NOCTR           | Montant HT hors prix tarif client      |
| lignes          | TTC_NOCTR          | Montant TTC hors prix tarif client     |
| lignes          | PRIXPAR            |                                        |
| lignes          | CATPRODUCT_LABEL   | Libellé catégorie produit              |
| lignes          | PRODUCTLOGO        | Logo Produit                           |
| lignes          | CLASSIF            | Classification produit                 |
| lignes          | TVA5               | Montant TVA 5% sur ligne               |
| lignes          | TVA10              | Montant TVA 10% sur ligne              |
| lignes          | TVA20              | Montant TVA 20% sur ligne              |
| detailtva       | TAUX               | Taux de TVA                            |
| detailtva       | HT                 | Montant Hors Taxes TVA                 |
| detailtva       | TVA                | Montant TVA                            |
