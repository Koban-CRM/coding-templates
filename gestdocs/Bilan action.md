Modèle de document Bilan d'action

Voici le code correspondant à la déclaration des champs d'un modèle de document Bilan d'action.

**Version Compatible** : Décembre 2026 et supérieures

```xml
 <DataSets>
    <DataSet Name="contrat">
      <Fields>
        <Field Name="FROM">
          <DataField>FROM</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="TO">
          <DataField>TO</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="LABEL">
          <DataField>LABEL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NUMBER">
          <DataField>NUMBER</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="tiers">
      <Fields>
        <Field Name="LABEL">
          <DataField>LABEL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="EXTERNALCODE">
          <DataField>EXTERNALCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="COMPLEMENT">
          <DataField>COMPLEMENT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="STREET">
          <DataField>STREET</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CITY">
          <DataField>CITY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ZIPCODE">
          <DataField>ZIPCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="COUNTRY">
          <DataField>COUNTRY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PHONE">
          <DataField>PHONE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="tiersparent">
      <Fields>
        <Field Name="LABEL">
          <DataField>LABEL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="EXTERNALCODE">
          <DataField>EXTERNALCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="COMPLEMENT">
          <DataField>COMPLEMENT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="STREET">
          <DataField>STREET</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="CITY">
          <DataField>CITY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ZIPCODE">
          <DataField>ZIPCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="COUNTRY">
          <DataField>COUNTRY</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PHONE">
          <DataField>PHONE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="action">
      <Fields>
        <Field Name="FROM">
          <DataField>FROM</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="TO">
          <DataField>TO</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="LABEL">
          <DataField>LABEL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ACTIONTYPE">
          <DataField>ACTIONTYPE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="ASSIGNEDTO">
          <DataField>ASSIGNEDTO</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="COMMENTS">
          <DataField>COMMENTS</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="signataire">
      <Fields>
        <Field Name="NAME">
          <DataField>NAME</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="FIRSTNAME">
          <DataField>FIRSTNAME</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="EMAIL">
          <DataField>EMAIL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="bilan">
      <Fields>
        <Field Name="OSCODE">
          <DataField>OSCODE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="OSLABEL">
          <DataField>OSLABEL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="BILANDATE">
          <DataField>BILANDATE</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="FEELING">
          <DataField>FEELING</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="STATUS">
          <DataField>STATUS</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="SIGNATURE">
          <DataField>SIGNATURE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="F_6a99127af0415da0bb951b27">
          <DataField>F_6a99127af0415da0bb951b27</DataField>
          <rd:TypeName>System.Boolean</rd:TypeName>
        </Field>
        <Field Name="F_6a5f3010b75f9fe85b74b605">
          <DataField>F_6a5f3010b75f9fe85b74b605</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="F_6a5f3019b75f9fe85b74b681">
          <DataField>F_6a5f3019b75f9fe85b74b681</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="F_6a5f3023b75f9fe85b74b6ef">
          <DataField>F_6a5f3023b75f9fe85b74b6ef</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="F_6a5f302fb75f9fe85b74b794">
          <DataField>F_6a5f302fb75f9fe85b74b794</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="F_6a5f3045b75f9fe85b74b8b2">
          <DataField>F_6a5f3045b75f9fe85b74b8b2</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="F_6a5f304fb75f9fe85b74b92d">
          <DataField>F_6a5f304fb75f9fe85b74b92d</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="F_6a5f30acb75f9fe85b74bd0e">
          <DataField>F_6a5f30acb75f9fe85b74bd0e</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="F_6a5f30b7b75f9fe85b74bd91">
          <DataField>F_6a5f30b7b75f9fe85b74bd91</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="F_6a9ae572ca6a63bb3f4fa9e7">
          <DataField>F_6a9ae572ca6a63bb3f4fa9e7</DataField>
          <rd:TypeName>System.Boolean</rd:TypeName>
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



| Nom DataSet | Nom Champ                  | Définition                                                 |
| ----------- | -------------------------- | ---------------------------------------------------------- |
| contrat     | FROM                       | Date de début du contrat                                   |
| contrat     | TO                         | Date de fin du contrat                                     |
| contrat     | LABEL                      | Libellé du contrat                                         |
| contrat     | NUMBER                     | Numéro du contrat                                          |
| tiers       | LABEL                      | Nom du tiers                                               |
| tiers       | EXTERNALCODE               | Code externe du tiers                                      |
| tiers       | COMPLEMENT                 | Adresse / Complément du tiers                              |
| tiers       | STREET                     | Adresse / Rue du tiers                                     |
| tiers       | CITY                       | Adresse / Ville du tiers                                   |
| tiers       | ZIPCODE                    | Adresse / Code postal du tiers                             |
| tiers       | COUNTRY                    | Adresse / Pays du tiers                                    |
| tiers       | PHONE                      | Téléphone du tiers                                         |
| tiersparent | LABEL                      | Nom du tiers parent                                        |
| tiersparent | EXTERNALCODE               | Code externe du tiers parent                               |
| tiersparent | COMPLEMENT                 | Adresse / Complément du tiers parent                       |
| tiersparent | STREET                     | Adresse / Rue du tiers parent                              |
| tiersparent | CITY                       | Adresse / Ville du tiers parent                            |
| tiersparent | ZIPCODE                    | Adresse / Code postal du tiers parent                      |
| tiersparent | COUNTRY                    | Adresse / Pays du tiers parent                             |
| tiersparent | PHONE                      | Téléphone du tiers parent                                  |
| action      | FROM                       | Date de début de l'action                                  |
| action      | TO                         | Date de fin de l'action                                    |
| action      | LABEL                      | Libellé de l'action                                        |
| action      | ACTIONTYPE                 | Type d'action                                              |
| action      | ASSIGNEDTO                 | Personne à qui l'action est assignée                       |
| action      | COMMENTS                   | Commentaires de l'action                                   |
| signataire  | NAME                       | Nom du signataire                                          |
| signataire  | FIRSTNAME                  | Prénom du signataire                                       |
| signataire  | EMAIL                      | Adresse e-mail du signataire                               |
| bilan       | OSCODE                     | Code de l'objectif / du suivi (OS)                         |
| bilan       | OSLABEL                    | Libellé de l'objectif / du suivi (OS)                      |
| bilan       | BILANDATE                  | Date du bilan                                              |
| bilan       | FEELING                    | Ressenti                                                   |
| bilan       | STATUS                     | Statut du bilan                                            |
| bilan       | SIGNATURE                  | Signature                                                  |
| bilan       | F_6a99127af0415da0bb951b27 | Champ personnalisé (à compléter avec identifiant du champ) |
|             |                            |                                                            |
|             |                            |                                                            |
|             |                            |                                                            |
|             |                            |                                                            |
|             |                            |                                                            |
|             |                            |                                                            |
|             |                            |                                                            |
|             |                            |                                                            |
|             |                            |                                                            |


