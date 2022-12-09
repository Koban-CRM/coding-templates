# Modèle de document Bon de commande

Voici le code correspondant  à la déclaration des champs d'un modèle de document Bon de commande.

**Version Compatible** : Février 2022 et supérieures

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
        <Field Name="ADRDEL_NOM">
          <DataField>ADRDEL_NOM</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRDEL_PRENOM">
          <DataField>ADRDEL_PRENOM</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRDEL_TEL">
          <DataField>ADRDEL_TEL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRDEL_COMPLEMENT">
          <DataField>ADRDEL_COMPLEMENT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRDEL_RUE">
          <DataField>ADRDEL_RUE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRDEL_VILLE">
          <DataField>ADRDEL_VILLE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRDEL_CPOSTAL">
          <DataField>ADRDEL_CPOSTAL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ACCOUNTINGCODE">
          <DataField>ACCOUNTINGCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADR_COUNTRY">
          <DataField>ADR_COUNTRY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRDEL_COUNTRY">
          <DataField>ADRDEL_COUNTRY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NOTVA">
          <DataField>NOTVA</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="EXTCODE">
          <DataField>EXTCODE</DataField>
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
        <Field Name="BANK">
          <DataField>BANK</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PRENOM">
          <DataField>PRENOM</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="GENDER">
          <DataField>GENDER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="OFFICIALNUMBER">
          <DataField>OFFICIALNUMBER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="OFFICIALNUMBER">
          <DataField>OFFICIALNUMBER</DataField>
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
        <Field Name="ADRFAC_CPOSTAL">
          <DataField>ADRFAC_CPOSTAL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADRFAC_COUNTRY">
          <DataField>ADRFAC_COUNTRY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="commande">
      <Fields>
        <Field Name="DATECOMMANDE">
          <DataField>DATECOMMANDE</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="TELPAR">
          <DataField>TELPAR</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="EMAILPAR">
          <DataField>EMAILPAR</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="LOGO">
          <DataField>LOGO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PIEDPAGE">
          <DataField>PIEDPAGE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NUMERO">
          <DataField>NUMERO</DataField>
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
        <Field Name="BACKCOLOR">
          <DataField>BACKCOLOR</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PERIODEVALIDITE">
          <DataField>PERIODEVALIDITE</DataField>
          <rd:TypeName>System.Int32</rd:TypeName>
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
        <Field Name="REFCLIENT">
          <DataField>REFCLIENT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CURRENCYSYMBOL">
          <DataField>CURRENCYSYMBOL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="MAILCONTACT">
          <DataField>MAILCONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TELCONTACT">
          <DataField>TELCONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="LABELECHEANCE">
          <DataField>LABELECHEANCE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NODEVIS">
          <DataField>NODEVIS</DataField>
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
        <Field Name="THIRDLOGO">
          <DataField>THIRDLOGO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DEVISPERIODEVALIDITE">
          <DataField>DEVISPERIODEVALIDITE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DEVISDATELIVRAISON">
          <DataField>DEVISDATELIVRAISON</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="DEVISDUREETRAVAUX">
          <DataField>DEVISDUREETRAVAUX</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PRENOMCONTACT">
          <DataField>PRENOMCONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="GENDERCONTACT">
          <DataField>GENDERCONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="LIBELLEDEVIS">
          <DataField>LIBELLEDEVIS</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="DATELIVRAISONESTIMEE">
          <DataField>DATELIVRAISONESTIMEE</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
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
        <Field Name="PRODUCTLOGO">
          <DataField>PRODUCTLOGO</DataField>
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
        <Field Name="PROVIDER">
          <DataField>PROVIDER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NOORDERPROVIDER">
          <DataField>NOORDERPROVIDER</DataField>
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

