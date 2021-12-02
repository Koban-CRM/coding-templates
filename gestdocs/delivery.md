# Modèle de document Bon de livraison

Voici le code correspondant  à la déclaration des champs d'un modèle de document Bon de livraison.

**Version Compatible** : Décembre 2021 et supérieures

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
        <Field Name="ADR_CONTACT">
          <DataField>ADR_CONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ADR_PHONE">
          <DataField>ADR_PHONE</DataField>
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
        <Field Name="DATEDELIVERY">
          <DataField>DATEDELIVERY</DataField>
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
        <Field Name="HEADER">
          <DataField>HEADER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="FOOTER">
          <DataField>FOOTER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NOORDER">
          <DataField>NOORDER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NOCUSTORDER">
          <DataField>NOCUSTORDER</DataField>
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
        <Field Name="NBPACK">
          <DataField>NBPACK</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="TOTALWEIGHT">
          <DataField>TOTALWEIGHT</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="PHONECONTACT">
          <DataField>PHONECONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="MAILCONTACT">
          <DataField>MAILCONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NODEVIS">
          <DataField>NODEVIS</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="COMMENT">
          <DataField>COMMENT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="LABELDEVIS">
          <DataField>LABELDEVIS</DataField>
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
        <Field Name="QUANTITE">
          <DataField>QUANTITE</DataField>
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
        <Field Name="REGPRODUCT">
          <DataField>REGPRODUCT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CATPRODUCT">
          <DataField>CATPRODUCT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ORDERQUANTITE">
          <DataField>ORDERQUANTITE</DataField>
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
  </DataSets>
```

## Définition des champs

| Nom DataSet | Nom Champ           | Définition                            |
| ----------- | ------------------- | ------------------------------------- |
| client      | NOM                 | Nom du fournisseur                    |
| client      | ADR_COMPLEMENT      | Adresse / Complément Fournisseur      |
| client      | ADR_NOVOIE          | Non utilisé                           |
| client      | ADR_RUE             | Adresse / Rue Fournisseur             |
| client      | ADR_VILLE           | Adresse / Ville Fournisseur           |
| client      | ADR_CPOSTAL         | Adresse / Code Postal Fournisseur     |
| client      | ADR_CONTACT         | Adresse / Nom du contact              |
| client      | ADR_PHONE           | Adresse / Téléphone                   |
| client      | ACCOUNTINGCODE      | Compte comptable                      |
| client      | EXTCODE             | Code externe                          |
| client      | SPECFIELD1          | Champ personnalisé 1                  |
| client      | SPECFIELD2          | Champ personnalisé 2                  |
| client      | ADR_COUNTRY         | Adresse / Pays                        |
| client      | ADRFAC_COMPLEMENT   | Adresse de facturation / Complément   |
| client      | ADRFAC_RUE          | Adresse de facturation / Rue          |
| client      | ADRFAC_VILLE        | Adresse de facturation / Ville        |
| client      | ADRFAC_CPOSTAL      | Adresse de facturation / Code postal  |
| client      | ADRFAC_COUNTRY      | Adresse de facturation / Pays         |
| commande    | DATEDELIVERY        | Date du bon de livraison              |
| commande    | TELPAR              | Téléphone personne affectée           |
| commande    | EMAILPAR            | EMail personne affectée               |
| commande    | LOGO                | Logo structure                        |
| commande    | PIEDPAGE            | Texte Pied de page                    |
| commande    | NUMERO              | Numéro Commande Fournisseur           |
| commande    | PAR                 | Nom et prénom personne affectée       |
| commande    | NOMCONTACT          | Nom du contact fournisseur            |
| commande    | BACKCOLOR           | Couleur de fond du modèle de document |
| commande    | HEADER              |                                       |
| commande    | FOOTER              | Mode de règlement                     |
| commande    | NOORDER             | Dépot                                 |
| commande    | NOMSOCIETE          | Nom Structure                         |
| commande    | FORMECAPITAL        | Forme Capital Structure               |
| commande    | ADRESSE1            | Adresse 1 Structure                   |
| commande    | ADRESSE2            | Adresse 2 Structure                   |
| commande    | SIREN               | SIREN Structure                       |
| commande    | RCS                 | Non utilisé                           |
| commande    | APE                 | Non utilisé                           |
| commande    | NOTVA               | Numéro TVA Structure                  |
| commande    | MENTIONCOMPL        | Mentions complémentaire Structure     |
| commande    | NBPACK              | Nombre de colis                       |
| commande    | TOTALWEIGHT         | Poids total                           |
| commande    | PHONECONTACT        | Téléphone du contact                  |
| commande    | MAILCONTACT         | Mail du contact                       |
| commande    | NODEVIS             | Numéro de devis initial               |
| commande    | COMMENT             | Commentaire bon de livraison          |
| commande    | LABELDEVIS          | Libellé du devis initial              |
| commande    | MOBILECONTACT       | Mobile du contact                     |
| lignes      | REFERENCE           | Libellé ligne                         |
| lignes      | COMMENTAIRE         | Commentaire ligne                     |
| lignes      | UNITE               | Unité                                 |
| lignes      | QUANTITE            | Quantité                              |
| lignes      | REFPRODUCT          | Référence Produit interne             |
| lignes      | BARCODE             | Code Barre                            |
| lignes      | SECTIONID           | Identifiant Section                   |
| lignes      | LIBELLE             | Libellé Section                       |
| lignes      | COMMENTAIRE_SECTION | Commentaire section                   |
| lignes      | REGPRODUCT          | Regroupement de produit               |
| lignes      | CATPRODUCT          | Catégorie de produit                  |
| lignes      | ORDERQUANTITE       | Quantité initiale commande            |
| lignes      | CF1                 | Champ Extension 1                     |
| lignes      | CF2                 | Champ Extension 2                     |

## DataSet Objet personnalisé

Dans un bon de livraison, vous pouvez insérer un dataset pour chaque objet personnalisé possible.

Le DataSet à insérer va prendre cette forme :

```xml
<DataSet Name="OD_XXXXXXXXXXXX">
      <Fields>
        <Field Name="PRODUCTCODE">
          <DataField>PRODUCTCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PRODUCTLABEL">
          <DataField>PRODUCTLABEL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="YYYYYYYYYYYYY">
          <DataField>YYYYYYYYYYYYY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ZZZZZZZZZZZZZ">
          <DataField>ZZZZZZZZZZZZZ</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
```

Le nom du DataSet doit prendre comme valeur **OD_** suivi de l'**identifiant de l'objet personnalisé**.

Chaque champ personnalisé de l'objet doit être ajouté dans le DataSet. Le nom du champ doit être l'**identifiant du champ personnalisé** dans Koban.