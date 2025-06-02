# Modèle de document Fiche OPPPORTUNITÉ

Voici le code correspondant  à la déclaration des champs d'un modèle de document Objet spécifique.

**Version Compatible** : Juin 2025 et supérieures

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
        <Field Name="EMAIL">
          <DataField>EMAIL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="Affecte">
          <DataField>AFFECTEA</DataField>
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
        <Field Name="ETAPE">
          <DataField>ETAPE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="PROBABILITE">
          <DataField>PROBABILITE</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="CAPREVISIONNEL">
          <DataField>CAPREVISIONNEL</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="DATEPREVISION">
          <DataField>DATEPREVISION</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="RESPONSABLE">
          <DataField>RESPONSABLE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NOMCONTACT">
          <DataField>NOMCONTACT</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
  <Field Name="Detail_des_activites">
          <DataField>f_683d51998172f5287c6c7e4e</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
     <Field Name="Transport_inclus">
          <DataField>f_683d4f8e8172f5287c6c7e3f</DataField>
          <rd:TypeName>System.Boolean</rd:TypeName>
        </Field>
     <Field Name="Nombre_de_participants">
          <DataField>f_683d4f1e8172f5287c6c7e3cb</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
     <Field Name="date_de_l_evenement">
          <DataField>f_683d4bc08172f5287c6c7e19</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
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



| Nom DataSet | Nom Champ              | Définition                                                                           |
|:-----------:| ---------------------- | ------------------------------------------------------------------------------------ |
| client      | ADR_RUE                | Adresse / Rue  client                                                                |
| client      | ADR_VILLE              | Adresse /  Ville client                                                              |
| client      | ADR_CPOSTAL            | Adresse /  Code Postal client                                                        |
| client      | ADR_COUNTRY            | Adresse /  Pays client                                                               |
| client      | PHONE                  | Téléphone  client                                                                    |
| client      | EMAIL                  | Email client                                                                         |
| opportunite | LIBELLE                | Libellé opportunité                                                                  |
| opportunite | ETAPE                  | Etape processus                                                                      |
| opportunite | PROBABILITE            | Probabilité (En %)                                                                   |
| opportunite | CAPREVISIONNEL         | Montant                                                                              |
| opportunite | DATEPREVISION          | Date de décision                                                                     |
| opportunite | RESPONSABLE            | Personne affectée                                                                    |
| opportunite | NOMCONTACT             | Nom contact client                                                                   |
| opportunite | Detail_des_activites   | Champ personnalisé Koban (id du champ) de type System string(Format caractères)      |
| opportunite | Transport_inclus       | Champ personnalisé Koban (id du champ) de type System.Boolean (Format case à cocher) |
| opportunite | Date_de_l_evenement    | Champ personnalisé Koban (id du champ) de type System.DateTime (Format date)         |
| opportunite | Nombre_de_participants | Champ personnalisé Koban (id du champ) de type System.Double (Format numérique)      |
