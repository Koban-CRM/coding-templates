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

## Définition des champs

| Nom DataSet     | Nom Champ            | Définition                             |
| --------------- | -------------------- | -------------------------------------- |
| client          | NOM                  | Nom du fournisseur                     |
| client          | ADR_COMPLEMENT       | Adresse / Complément Fournisseur       |
| client          | ADR_NOVOIE           | Non utilisé                            |
| client          | ADR_RUE              | Adresse / Rue Fournisseur              |
| client          | ADR_VILLE            | Adresse / Ville Fournisseur            |
| client          | ADR_CPOSTAL          | Adresse / Code Postal Fournisseur      |
| client          | ADR_COUNTRY          | Adresse / Pays Fournisseur             |
| client          | ADRDEL_NOM           | Adresse Livraison / Nom Client         |
| client          | ADRDEL_PRENOM        | Adresse Livraison / Prénom Client      |
| client          | ADRDEL_TEL           | Adresse Livraison / Téléphone Client   |
| client          | ADRDEL_COMPLEMENT    | Adresse Livraison / Complément Client  |
| client          | ADRDEL_RUE           | Adresse Livraison / Rue Client         |
| client          | ADRDEL_VILLE         | Adresse Livraison / Ville Client       |
| client          | ADRDEL_CPOSTAL       | Adresse Livraison / Code Postal Client |
| client          | ADRDEL_COUNTRY       | Adresse Livraison / Pays Client        |
| client          | NOTVA                | Numéro TVA Structure                   |
| client          | ACCOUNTINGCODE       | Compte comptable client                |
| client          | EXTCODE              | Code externe client                    |
| client          | RIB                  | RIB Structure                          |
| client          | IBAN                 | IBAN Structure                         |
| client          | BIC                  | BIC Structure                          |
| client          | BANK                 | Banque                                 |
| client          | ADRFAC_COMPLEMENT    | Adresse de facturation / Complément    |
| client          | ADRFAC_RUE           | Adresse de facturation / Rue           |
| client          | ADRFAC_VILLE         | Adresse de facturation / Ville         |
| client          | ADRFAC_CP            | Adresse de facturation / Code postal   |
| client          | ADRFAC_COUNTRY       | Adresse de facturation / Pays          |
| commande        | DATECOMMANDE         | Date de la commande fournisseur        |
| commande        | TELPAR               | Téléphone personne affectée            |
| commande        | EMAILPAR             | EMail personne affectée                |
| commande        | LOGO                 | Logo structure                         |
| commande        | PIEDPAGE             | Texte Pied de page                     |
| commande        | NUMERO               | Numéro Commande Fournisseur            |
| commande        | PAR                  | Nom et prénom personne affectée        |
| commande        | NOMCONTACT           | Nom du contact fournisseur             |
| commande        | BACKCOLOR            | Couleur de fond du modèle de document  |
| commande        | PERIODEVALIDITE      | Période de validité                    |
| commande        | MODERGLT             | Mode de règlement                      |
| commande        | NOMSOCIETE           | Nom Structure                          |
| commande        | FORMECAPITAL         | Forme Capital Structure                |
| commande        | ADRESSE1             | Adresse 1 Structure                    |
| commande        | ADRESSE2             | Adresse 2 Structure                    |
| commande        | SIREN                | SIREN Structure                        |
| commande        | RCS                  | Non utilisé                            |
| commande        | APE                  | Non utilisé                            |
| commande        | NOTVA                | Numéro TVA Structure                   |
| commande        | MENTIONCOMPL         | Mentions complémentaire Structure      |
| commande        | HEADER               | Texte Entête                           |
| commande        | FOOTER               | Texte Pied de page                     |
| commande        | CURRENCYSYMBOL       | Devise                                 |
| commande        | MAILCONTACT          | Email contact client                   |
| commande        | TELCONTACT           | SIREN Structure                        |
| commande        | LABELECHEANCE        | Libellé échéance                       |
| commande        | NODEVIS              | N° de devis                            |
| commande        | EMAILAFFECTE         | EMail personne affectée                |
| commande        | NOMAFFECTE           | Personne affectée                      |
| commande        | MOBILEAFFECTE        | Mobile personne affectée               |
| commande        | THIRDLOGO            | Logo structure                         |
| commande        | DEVISPERIODEVALIDITE | Durée de validité devis                |
| commande        | DEVISDATELIVRAISON   | Date de livraion devis                 |
| commande        | DEVISDUREETRAVAUX    | Durée des travaux devis                |
| commande        | PRENOMCONTACT        | Prénom contact client                  |
| commande        | GENDERCONTACT        | Civilité Contact client                |
| commande        | LIBELLEDEVIS         | Libellé devis                          |
| commande        | DATELIVRAISONESTIMEE | Date de livraison client estimée       |
| opportspecfield | SPECFIELD1           | Non utilisé                            |
| opportspecfield | SPECFIELD2           | Non utilisé                            |
| opportspecfield | SPECFIELD3           | Non utilisé                            |
| opportspecfield | SPECFIELD4           | Non utilisé                            |
| opportspecfield | SPECFIELD5           | Non utilisé                            |
| opportspecfield | SPECFIELD6           | Non utilisé                            |
| lignes          | REFERENCE            | Libellé ligne                          |
| lignes          | COMMENTAIRE          | Commentaire ligne                      |
| lignes          | UNITE                | Unité                                  |
| lignes          | PRIXUNITAIRE         | Prix unitaire                          |
| lignes          | HT                   | Montant HT                             |
| lignes          | QUANTITE             | Quantité                               |
| lignes          | REDUCTION            | Réduction                              |
| lignes          | TTC                  | Montant TTC                            |
| lignes          | TVA                  | Montant TVA                            |
| lignes          | REFPRODUCT           | Référence Produit interne              |
| lignes          | BARCODE              | Code barre                             |
| lignes          | SECTIONID            | Identifiant section                    |
| lignes          | LIBELLE              | Libellé section                        |
| lignes          | COMMENTAIRESECTION   | Commentaire section                    |
| lignes          | ISCTR                | Est un produit avec tarif client       |
| lignes          | HT_PUCTR             | Montant HT prix tarif client           |
| lignes          | TTC_PUCTR            | Montant TTC prix tarif client          |
| lignes          | HT_NOCTR             | Montant HT hors prix tarif client      |
| lignes          | TTC_NOCTR            | Montant TTC hors prix tarif client     |
| lignes          | PRIXPAR              |                                        |
| lignes          | CATPRODUCT_LABEL     | Libellé catégorie produit              |
| lignes          | PRODUCTLOGO          | Logo Produit                           |
| lignes          | CLASSIF              | Classification produit                 |
| lignes          | TVA5                 | Montant TVA 5% sur ligne               |
| lignes          | TVA10                | Montant TVA 10% sur ligne              |
| lignes          | TVA20                | Montant TVA 20% sur ligne              |
| lignes          | PACKING              |                                        |
| detailtva       | TAUX                 | Taux de TVA                            |
| detailtva       | HT                   | Montant Hors Taxes TVA                 |
| detailtva       | TVA                  | Montant TVA                            |
