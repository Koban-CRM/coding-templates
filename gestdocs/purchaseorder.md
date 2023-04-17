# Modèle de document Bon de commande Fournisseur

Voici le code correspondant  à la déclaration des champs d'un modèle de document Bon de commande fournisseur.

**Version Compatible** : Octobre 2021 2.0 et supérieures

## DataSet

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
        <Field Name="ADR_COUNTRY">
          <DataField>ADR_COUNTRY</DataField>
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
        <Field Name="DEPOSIT">
          <DataField>DEPOSIT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NOCUSTORDER">
          <DataField>NOCUSTORDER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NOPROVIDER">
          <DataField>NOPROVIDER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CURRENCYSYMBOL">
          <DataField>CURRENCYSYMBOL</DataField>
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
        <Field Name="DELIVERYDATEESTIMATED">
          <DataField>DELIVERYDATEESTIMATED</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="CUSTORDER_NOM">
          <DataField>CUSTORDER_NOM</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CUSTORDER_ADR_COMPLEMENT">
          <DataField>CUSTORDER_ADR_COMPLEMENT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CUSTORDER_ADR_STREET">
          <DataField>CUSTORDER_ADR_STREET</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CUSTORDER_ADR_CITY">
          <DataField>CUSTORDER_ADR_CITY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CUSTORDER_ADR_ZIPCODE">
          <DataField>CUSTORDER_ADR_ZIPCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CUSTORDER_ADR_COUNTRY">
          <DataField>CUSTORDER_ADR_COUNTRY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="MENTIONCOMPL">
          <DataField>MENTIONCOMPL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CUSTORDER_ADRLIV_COMPLEMENT">
          <DataField>CUSTORDER_ADRLIV_COMPLEMENT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CUSTORDER_ADRLIV_STREET">
          <DataField>CUSTORDER_ADRLIV_STREET</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CUSTORDER_ADRLIV_CITY">
          <DataField>CUSTORDER_ADRLIV_CITY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CUSTORDER_ADRLIV_ZIPCODE">
          <DataField>CUSTORDER_ADRLIV_ZIPCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CUSTORDER_ADRLIV_COUNTRY">
          <DataField>CUSTORDER_ADRLIV_COUNTRY</DataField>
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
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="REFPRODUCTPROVIDER">
          <DataField>REFPRODUCTPROVIDER</DataField>
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

| Nom DataSet | Nom Champ                   | Définition                                                                             |
| ----------- | --------------------------- | -------------------------------------------------------------------------------------- |
| client      | NOM                         | Nom du fournisseur                                                                     |
| client      | ADR_COMPLEMENT              | Adresse / Complément Fournisseur                                                       |
| client      | ADR_NOVOIE                  | Non utilisé                                                                            |
| client      | ADR_RUE                     | Adresse / Rue Fournisseur                                                              |
| client      | ADR_VILLE                   | Adresse / Ville Fournisseur                                                            |
| client      | ADR_CPOSTAL                 | Adresse / Code Postal Fournisseur                                                      |
| client      | ADR_COUNTRY                 | Adresse / Pays Fournisseur                                                             |
| commande    | DATECOMMANDE                | Date de la commande fournisseur                                                        |
| commande    | TELPAR                      | Téléphone personne affectée                                                            |
| commande    | EMAILPAR                    | EMail personne affectée                                                                |
| commande    | LOGO                        | Logo structure                                                                         |
| commande    | PIEDPAGE                    | Texte Pied de page                                                                     |
| commande    | NUMERO                      | Numéro Commande Fournisseur                                                            |
| commande    | PAR                         | Nom et prénom personne affectée                                                        |
| commande    | NOMCONTACT                  | Nom du contact fournisseur                                                             |
| commande    | BACKCOLOR                   | Couleur de fond du modèle de document                                                  |
| commande    | PERIODEVALIDITE             | Période de validité                                                                    |
| commande    | MODERGLT                    | Mode de règlement                                                                      |
| commande    | DEPOSIT                     | Dépot                                                                                  |
| commande    | NOCUSTORDER                 | Numéro commande client                                                                 |
| commande    | NOPROVIDER                  | Numéro commande fournisseur                                                            |
| commande    | CURRENCYSYMBOL              | Devise                                                                                 |
| commande    | NOMSOCIETE                  | Nom Structure                                                                          |
| commande    | FORMECAPITAL                | Forme Capital Structure                                                                |
| commande    | ADRESSE1                    | Adresse 1 Structure                                                                    |
| commande    | ADRESSE2                    | Adresse 2 Structure                                                                    |
| commande    | SIREN                       | SIREN Structure                                                                        |
| commande    | RCS                         | Non utilisé                                                                            |
| commande    | APE                         | Non utilisé                                                                            |
| commande    | NOTVA                       | Numéro TVA Structure                                                                   |
| commande    | MENTIONCOMPL                | Mentions complémentaire Structure                                                      |
| commande    | DELIVERYDATEESTIMATED       | Date de livraison estimée                                                              |
| commande    | CUSTORDER_NOM               | Nom du client de la commande client liée à la commande fournisseur                     |
| commande    | CUSTORDER_ADR_COMPLEMENT    | Adresse - Complément du client de la commande client liée à la commande fournisseur    |
| commande    | CUSTORDER_ADR_STREET        | Adresse - Rue du client de la commande client liée à la commande fournisseur           |
| commande    | CUSTORDER_ADR_CITY          | Adresse - Ville du client de la commande client liée à la commande fournisseur         |
| commande    | CUSTORDER_ADR_ZIPCODE       | Adresse - Code postal du client de la commande client liée à la commande fournisseur   |
| commande    | CUSTORDER_ADR_COUNTRY       | Adresse - Pays du client de la commande client liée à la commande fournisseur          |
| commande    | CUSTORDER_ADRLIV_COMPLEMENT | Adresse de livraison - Complément de la commande client liée à la commande fournisseur |
| commande    | CUSTORDER_ADRLIV_STREET     | Adresse de livraison - Rue de la commande client liée à la commande fournisseur        |
| commande    | CUSTORDER_ADRLIV_CITY       | Adresse de livraison - Ville de la commande client liée à la commande fournisseur      |
| commande    | CUSTORDER_ADRLIV_ZIPCODE    | Adresse de livraison -Code postal de la commande client liée à la commande fournisseur |
| commande    | CUSTORDER_ADRLIV_COUNTRY    | Adresse de livraison - Pays de la commande client liée à la commande fournisseur       |
| lignes      | REFERENCE                   | Libellé produit                                                                        |
| lignes      | COMMENTAIRE                 | Commentaire produit                                                                    |
| lignes      | UNITE                       | Unité                                                                                  |
| lignes      | PRIXUNITAIRE                | Prix unitaire                                                                          |
| lignes      | HT                          | Montant HT                                                                             |
| lignes      | QUANTITE                    | Quantité                                                                               |
| lignes      | REDUCTION                   | Réduction                                                                              |
| lignes      | TTC                         | Montant TTC                                                                            |
| lignes      | TVA                         | Montant TVA                                                                            |
| lignes      | REFPRODUCT                  | Référence Produit interne                                                              |
| lignes      | REFPRODUCTPROVIDER          | Référence Produit Fournisseur (Code fournisseur)                                       |
