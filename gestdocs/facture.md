# Modèle de document Facture

Voici le code correspondant à la déclaration des champs d'un modèle de document Facture.

**Version Compatible** : Octobre 2021 2.0 et supérieures

## DataSet

------

------

- RDL Facture client

------

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
        <Field Name="NOTVA">
          <DataField>NOTVA</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CONTACTNAME">
          <DataField>CONTACTNAME</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CONTACTFIRSTNAME">
          <DataField>CONTACTFIRSTNAME</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ORIG_NOM">
          <DataField>ORIG_NOM</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ORIG_ADR_COMPLEMENT">
          <DataField>ORIG_ADR_COMPLEMENT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ORIG_ADR_RUE">
          <DataField>ORIG_ADR_RUE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ORIG_ADR_VILLE">
          <DataField>ORIG_ADR_VILLE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ORIG_ADR_CPOSTAL">
          <DataField>ORIG_ADR_CPOSTAL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ISTTC">
          <DataField>ISTTC</DataField>
          <rd:TypeName>System.Boolean</rd:TypeName>
        </Field>
        <Field Name="ACCOUNTINGCODE">
          <DataField>ACCOUNTINGCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="EXTCODE">
          <DataField>EXTCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="SPECFIELD1">
          <DataField>SPECFIELD1</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="SPECFIELD2">
          <DataField>SPECFIELD2</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADR_COUNTRY">
          <DataField>ADR_COUNTRY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ORIG_NOTVA">
          <DataField>ORIG_NOTVA</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CUST_LOGO">
          <DataField>CUST_LOGO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CUST_SIRET">
          <DataField>CUST_SIRET</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="facture">
      <Fields>
        <Field Name="NOMCONTACT">
          <DataField>NOMCONTACT</DataField>
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
        <Field Name="AVOIR">
          <DataField>AVOIR</DataField>
          <rd:TypeName>System.Boolean</rd:TypeName>
        </Field>
        <Field Name="DATE">
          <DataField>DATE</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="ECHEANCE">
          <DataField>ECHEANCE</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="NOCOMMANDE">
          <DataField>NOCOMMANDE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="LABELOPPORTUNITE">
          <DataField>LABELOPPORTUNITE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NODEVIS">
          <DataField>NODEVIS</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NOCOMMANDECLIENT">
          <DataField>NOCOMMANDECLIENT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="LOGO">
          <DataField>LOGO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ACOMPTEHT">
          <DataField>ACOMPTEHT</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="ACOMPTETVA">
          <DataField>ACOMPTETVA</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="ACOMPTETTC">
          <DataField>ACOMPTETTC</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="PIEDPAGE">
          <DataField>PIEDPAGE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NUMERO">
          <DataField>NUMERO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="BACKCOLOR">
          <DataField>BACKCOLOR</DataField>
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
        <Field Name="HEADER">
          <DataField>HEADER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="FOOTER">
          <DataField>FOOTER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ISPAYED">
          <DataField>ISPAYED</DataField>
          <rd:TypeName>System.Boolean</rd:TypeName>
        </Field>
        <Field Name="CURRENCYSYMBOL">
          <DataField>CURRENCYSYMBOL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NODELIV">
          <DataField>NODELIV</DataField>
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
        <Field Name="CHPSUP1">
          <DataField>CHPSUP1</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CHPSUP2">
          <DataField>CHPSUP2</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CHPSUP3">
          <DataField>CHPSUP3</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CHPSUP4">
          <DataField>CHPSUP4</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CHPSUP5">
          <DataField>CHPSUP5</DataField>
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
        <Field Name="PAR">
          <DataField>PAR</DataField>
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
        <Field Name="TH_CHPSUP1">
          <DataField>TH_CHPSUP1</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TH_CHPSUP2">
          <DataField>TH_CHPSUP2</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TH_CHPSUP3">
          <DataField>TH_CHPSUP3</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TH_CHPSUP4">
          <DataField>TH_CHPSUP4</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TH_CHPSUP5">
          <DataField>TH_CHPSUP5</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TH_CHPSUP6">
          <DataField>TH_CHPSUP6</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PERIODFROM">
          <DataField>PERIODFROM</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="PERIODTO">
          <DataField>PERIODTO</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="HASH">
          <DataField>HASH</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TTCPAYED">
          <DataField>TTCPAYED</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="NBPACK">
          <DataField>NBPACK</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TOTALWEIGHT">
          <DataField>TOTALWEIGHT</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="PROCLOGO">
          <DataField>PROCLOGO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DEALPROCESS">
          <DataField>DEALPROCESS</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DEALPROCESS_VILLE">
          <DataField>DEALPROCESS_VILLE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="STEP">
          <DataField>STEP</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="STEPPERCENT">
          <DataField>STEPPERCENT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PRJ_DONE">
          <DataField>PRJ_DONE</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="PRJ_TOPAY">
          <DataField>PRJ_TOPAY</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="PRJ_TODO">
          <DataField>PRJ_TODO</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="CODEOPPORTUNITE">
          <DataField>CODEOPPORTUNITE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="QUOTE_LABEL">
          <DataField>QUOTE_LABEL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="IBAN_LABEL">
          <DataField>IBAN_LABEL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DEVISPERIODEVALIDITE">
          <DataField>DEVISPERIODEVALIDITE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DEVISDATELIVRAISON">
          <DataField>DEVISDATELIVRAISON</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DEVISDUREETRAVAUX">
          <DataField>DEVISDUREETRAVAUX</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="MOBILECONTACT">
          <DataField>MOBILECONTACT</DataField>
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
    <DataSet Name="echeances">
      <Fields>
        <Field Name="DATE">
          <DataField>DATE</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="HT">
          <DataField>HT</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="TTC">
          <DataField>TTC</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="facintermediaires">
      <Fields>
        <Field Name="NUMERO">
          <DataField>NUMERO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="INVOICEDATE">
          <DataField>INVOICEDATE</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="HT">
          <DataField>HT</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="TTC">
          <DataField>TTC</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="AMOUNTPAYED">
          <DataField>AMOUNTPAYED</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="MODEREGLT">
          <DataField>MODEREGLT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="faccommande">
      <Fields>
        <Field Name="NUMERO">
          <DataField>NUMERO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="INVOICEDATE">
          <DataField>INVOICEDATE</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="HT">
          <DataField>HT</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="TTC">
          <DataField>TTC</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="AMOUNTPAYED">
          <DataField>AMOUNTPAYED</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="MODEREGLT">
          <DataField>MODEREGLT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="LASTPAYMENTDATE">
          <DataField>LASTPAYMENTDATE</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="ISACOMPTE">
          <DataField>ISACOMPTE</DataField>
          <rd:TypeName>System.Boolean</rd:TypeName>
        </Field>
        <Field Name="ISASSET">
          <DataField>ISASSET</DataField>
          <rd:TypeName>System.Boolean</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="histoacompte">
      <Fields>
        <Field Name="NUMERO">
          <DataField>NUMERO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TTC">
          <DataField>TTC</DataField>
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
    <DataSet Name="lignes">
      <Fields>
        <Field Name="REFERENCE">
          <DataField>REFERENCE</DataField>
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
        <Field Name="REFPRODUCT">
          <DataField>REFPRODUCT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="BARCODE">
          <DataField>BARCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="SECTIONID">
          <DataField>SECTIONID</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="LIBELLE">
          <DataField>LIBELLE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="COMMENTAIRE_SECTION">
          <DataField>COMMENTAIRE_SECTION</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CATPRODUCT_LABEL">
          <DataField>CATPRODUCT_LABEL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ORDERQUANTITE">
          <DataField>ORDERQUANTITE</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="CUSTORDERREFERENCE">
          <DataField>CUSTORDERREFERENCE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PRODUCTLOGO">
          <DataField>PRODUCTLOGO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="HTTPS">
          <DataField>HTTPS</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
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
  </DataSets> Définition des champs
```

| Nom DataSet       | Nom Champ            | Définition                              |
| ----------------- | -------------------- | --------------------------------------- |
| client            | NOM                  | Nom du client                           |
| client            | ADR_COMPLEMENT       | Adresse / Complément client             |
| client            | ADR_NOVOIE           | Non utilisé                             |
| client            | ADR_RUE              | Adresse / Rue client                    |
| client            | ADR_VILLE            | Adresse / Ville client                  |
| client            | ADR_CPOSTAL          | Adresse / Code Postal client            |
| client            | ADR_COUNTRY          | Adresse / Pays client                   |
| client            | NOTVA                | N° TVA client                           |
| client            | CONTACTNAME          | Nom du contact client                   |
| client            | CONTACTFIRSTNAME     | Prénom du contact client                |
| client            | CONTACTEMAIL         | Email contact client                    |
| client            | ORIG_NOM             |                                         |
| client            | ORIG_ADR_COMPLEMENT  |                                         |
| client            | ORIG_ADR_RUE         |                                         |
| client            | ORIG_ADR_VILLE       |                                         |
| client            | ORIG_ADR_CPOSTA      |                                         |
| client            | ORIG_NOTVA           | N° de TVA du compte d'Origine           |
| client            | ISTTC                | Est TTC                                 |
| client            | ACCOUNTINGCODE       | Compte comptable client                 |
| client            | EXTCODE              | Code externe client                     |
| client            | SPECFIELD1           | Non utilisé                             |
| client            | SPECFIELD2           | Non utilisé                             |
| client            | CUST_SIRET           | N° SIRET client                         |
| client            | CUST_LOGO            | Logo client                             |
| facture           | NOMCONTACT           | Nom contact client                      |
| facture           | FAXCONTACT           | N° de fax contact client                |
| facture           | MAILCONTACT          | Email contact client                    |
| facture           | PHONECONTACT         | Télephone contact client                |
| facture           | AVOIR                | Avoir                                   |
| facture           | DATE                 | Date de Facture                         |
| facture           | ECHEANCE             | Échéance                                |
| facture           | NOCOMMANDE           | Numéro commande client                  |
| facture           | LABELOPPORTUNITE     | Libellé Opportunité                     |
| facture           | NODEVIS              | Numéro devis client                     |
| facture           | NOCOMMANDECLIENT     | Numéro commande externe client          |
| facture           | LOGO                 | Logo structure                          |
| facture           | ACOMPTEHT            | Montant hors taxes acompte              |
| facture           | ACOMPTETVA           | Montant TVA acompte                     |
| facture           | ACOMPTETTC           | Montant TTC acompte                     |
| facture           | PIEDPAGE             | Texte Pied de page                      |
| facture           | NUMERO               | Numéro Facture client                   |
| facture           | BACKCOLOR            | Couleur de fond du modèle de document   |
| facture           | MODERGLT             | Mode de règlement                       |
| facture           | NOMSOCIETE           | Nom Structure                           |
| facture           | FORMECAPITAL         | Forme Capital Structure                 |
| facture           | ADRESSE1             | Adresse 1 Structure                     |
| facture           | ADRESSE2             | Adresse 2 Structure                     |
| facture           | SIREN                | SIREN Structure                         |
| facture           | RCS                  | Non utilisé                             |
| facture           | APE                  | Non utilisé                             |
| facture           | NOTVA                | Numéro TVA Structure                    |
| facture           | MENTIONCOMPL         | Mentions complémentaire Structure       |
| facture           | HEADER               | Texte Entête                            |
| facture           | FOOTER               | Texte Pied de page                      |
| facture           | ISPAYED              | Statut soldé                            |
| facture           | CURRENCYSYMBOL       | Devise                                  |
| facture           | NODELIV              | N° bon de livraison                     |
| facture           | RIB                  | RIB Structure                           |
| facture           | IBAN                 | IBAN Structure                          |
| facture           | BIC                  | BIC Structure                           |
| facture           | DELIVCOMPL           | Adresse Livraison / Complément Client   |
| facture           | DELIVRUE             | Adresse Livraison / Rue Client          |
| facture           | DELIVVILLE           | Adresse Livraison / Ville Client        |
| facture           | DELIVCP              | Adresse Livraison / Code Postal Client  |
| facture           | PAR                  | Personne affectée                       |
| facture           | TELPAR               | Téléphone personne affectée             |
| facture           | EMAILPAR             | EMail personne affectée                 |
| facture           | TH_CHPSUP1           | Non utilisé                             |
| facture           | TH_CHPSUP2           | Non utilisé                             |
| facture           | TH_CHPSUP3           | Non utilisé                             |
| facture           | TH_CHPSUP4           | Non utilisé                             |
| facture           | TH_CHPSUP5           | Non utilisé                             |
| facture           | TH_CHPSUP6           | Non utilisé                             |
| facture           | PERIODFROM           | Date de début de période                |
| facture           | PERIODTO             | Date de fin de période                  |
| facture           | HASH                 | ID KOBAN                                |
| facture           | TTCPAYED             | Montant ttc payé                        |
| facture           | NBPACK               | Nombre de colis                         |
| facture           | TOTALWEIGHT          | Poids total                             |
| Immobilier        |                      |                                         |
| facture / adf     | PROCLOGO             | Logo programme                          |
| facture / adf     | DEALPROCESS          | Libellé programme                       |
| facture / adf     | DEALPROCESS_VILLE    | Ville programme                         |
| facture / adf     | STEP                 | Etape                                   |
| facture / adf     | STEPPERCENT          | Pourcentage étape                       |
| facture / adf     | PRJ_DONE             | Appel de fonds émis                     |
| facture / adf     | PRJ_TOPAY            | Appel de fond payer                     |
| facture / adf     | PRJ_TODO             | Appel de fonds à emettre                |
| facture           | CODEOPPORTUNITE      | Code opportunité                        |
| facture           | QUOTE_LABEL          | Libellé du devis initial                |
| facture           | IBAN_LABEL           | Libellé IBAN                            |
| facture           | DEVISPERIODEVALIDITE | Durée de validité devis                 |
| facture           | DEVISDATELIVRAISON   | Date de livraison devis                 |
| facture           | DEVISDUREETRAVAUX    | Durée des travaux devis                 |
| facture           | MOBILECONTACT        | N° de mobile du contact client          |
| detailtva         | TAUX                 | Taux de TVA                             |
| detailtva         | HT                   | Montant Hors Taxes TVA                  |
| detailtva         | TVA                  | Montant TVA                             |
| echeances         | DATE                 | Date d'écheance facture                 |
| echeances         | HT                   | Montant hors taxe de l'écheance         |
| echeances         | TTC                  | Montant TTC de l'écheance               |
| facintermediaires | NUMERO               | N° de facture intermediaire             |
| facintermediaires | INVOICEDATE          | Date de facture intermediaire           |
| facintermediaires | HT                   | Montant hors taxe facture intermediaire |
| facintermediaires | TTC                  | Montant TTC facture intermediaire       |
| facintermediaires | AMOUNTPAYED          | Montant payé facture intermediaire      |
| facintermediaires | MODEREGLT            | Mode de reglement facture intermediaire |
| faccommande       | NUMERO               | N° de commande                          |
| faccommande       | INVOICEDATE          | Date de commande                        |
| faccommande       | HT                   | Montant hors taxe commande              |
| faccommande       | TTC                  | Montant ttc commande                    |
| faccommande       | AMOUNTPAYED          | Montant payé commande                   |
| faccommande       | MODEREGLT            | Mode de reglement commande              |
| faccommande       | LASTPAYMENTDATE      | Date du dernier paiement                |
| faccommande       | ISACOMPTE            | Est un acompte                          |
| faccommande       | ISASSET              | Est un avoir                            |
| histoacompte      | NUMERO               | N° d'acompte                            |
| histoacompte      | TTC                  | Montant ttc acompte                     |
| histoacompte      | HT                   | Montant Hors Taxes acompte              |
| histoacompte      | TVA                  | TVA acompte                             |
| lignes            | REFERENCE            | Libellé ligne                           |
| lignes            | COMMENTAIRE          | Commentaire ligne                       |
| lignes            | UNITE                | Unité                                   |
| lignes            | PRIXUNITAIRE         | Prix unitaire                           |
| lignes            | HT                   | Montant HT                              |
| lignes            | QUANTITE             | Quantité                                |
| lignes            | REDUCTION            | Réduction                               |
| lignes            | TTC                  | Montant TTC                             |
| lignes            | TVA                  | Montant TVA                             |
| lignes            | REFPRODUCT           | Référence Produit interne               |
| lignes            | BARCODE              | Code barre                              |
| lignes            | SECTIONID            | Identifiant section                     |
| lignes            | LIBELLE              | Libellé ligne                           |
| lignes            | COMMENTAIRE_SECTION  | Commentaire section                     |
| lignes            | CATPRODUCT_LABEL     | Libellé catégorie produit               |
| lignes            | ORDERQUANTITE        | Quantité commandée                      |
| lignes            | CUSTORDERREFERENCE   | Référence client                        |
| lignes            | PRODUCTLOGO          | Logo Produit                            |
| lignes            | HTTPS                | URL boutique                            |
| lignes            | TVA5                 | Montant TVA 5% sur ligne                |
| lignes            | TVA10                | Montant TVA 10% sur ligne               |
| lignes            | TVA20                | Montant TVA 20% sur ligne               |
