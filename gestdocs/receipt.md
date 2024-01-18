Modèle de document Bon de réception

Voici le code correspondant à la déclaration des champs d'un modèle de document Bon de réception.

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
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
  </DataSets>
```

## Définition des champs

| Nom DataSet | Nom Champ      | Définition                            |
| ----------- | -------------- | ------------------------------------- |
| Client      | NOM            | Nom du client                         |
| client      | ADR_COMPLEMENT | Adresse / Complément client           |
| client      | ADR_NOVOIE     | Adresse / N° de rue client            |
| client      | ADR_RUE        | Adresse / Rue client                  |
| client      | ADR_VILLE      | Adresse / Ville client                |
| client      | ADR_CPOSTAL    | Adresse / Code Postal client          |
| commande    | DATEDELIVERY   | Date du bon de livraison              |
| commande    | TELPAR         | Téléphone personne affectée           |
| commande    | EMAILPAR       | EMail personne affectée               |
| commande    | LOGO           | Logo structure                        |
| commande    | PIEDPAGE       | Texte Pied de page                    |
| commande    | NUMERO         | Numéro Commande                       |
| commande    | PAR            | Nom et prénom personne affectée       |
| commande    | NOMCONTACT     | Nom du contact                        |
| commande    | BACKCOLOR      | Couleur de fond du modèle de document |
| commande    | HEADER         | Texte Entête                          |
| commande    | FOOTER         | Texte Pied de page                    |
| commande    | NOORDER        | Numéro de commande                    |
| lignes      | REFERENCE      | Libellé ligne                         |
| lignes      | COMMENTAIRE    | Commentaire ligne                     |
| lignes      | UNITE          | Unité                                 |
| lignes      | QUANTITE       | Quantité                              |
| lignes      | REFPRODUCT     | Référence Produit interne             |


