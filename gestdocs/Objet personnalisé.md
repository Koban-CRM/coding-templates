# Modèle de document OBJET PERSONNALISÉ

Voici le code correspondant  à la déclaration des champs d'un modèle de document Objet spécifique.

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
        <Field Name="EMAIL">
          <DataField>EMAIL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="Affecte">
          <DataField>AFFECTEA</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="NomObjet">
          <DataField>LIBELLE</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="fields">
      <Fields>
        <Field Name="date">
          <DataField>f_6451085e0dc3611e20f2d11b</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="equipementprotectionindiv">
          <DataField>f_6451088c0dc3611e20f2d156</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="maitrise_pitch">
          <DataField>f_6447c6120dc6ec187429d69e</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="rangement_coffre">
          <DataField>f_6447c6d40dc6ec187429d70e</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="equipt_protection_pi">
          <DataField>f_6451088c0dc3611e20f2d156</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="gadget">
          <DataField>f_64510f770dc3611e20f2d6b1</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="tournee_fixee">
          <DataField>f_6451106b0dc3611e20f2d77e</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="rdv_pris_recurrents">
          <DataField>f_645110860dc3611e20f2d794</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
 <Field Name="prochsession_posture">
          <DataField>f_646359380dc36114c424eff9</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
  <Field Name="n_de_serie">
          <DataField>f_67f4e44fc60d8b98c4e031c5</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="sous_garantie">
          <DataField>f_67f4e493c60d8b98c4e031e1</DataField>
          <rd:TypeName>System.Boolean</rd:TypeName>
        </Field>
        <Field Name="date_installation">
          <DataField>f_67f4e4abc60d8b98c4e031f6</DataField>
          <rd:TypeName>System.DateTime</rd:TypeName>
        </Field>
        <Field Name="prix_ht">
          <DataField>f_67f4ec85c60d8b98c4e03625</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="prix_ttc">
          <DataField>f_67f4e7a3c60d8b98c4e0335c</DataField>
          <rd:TypeName>System.Double</rd:TypeName>
        </Field>
        <Field Name="garantie">
          <DataField>f_67f4e50dc60d8b98c4e03231</DataField>
          <rd:TypeName>System.String</rd:TypeName>
      </Fields>
      <Query>
        <DataSourceName>Apeacz</DataSourceName>
        <CommandText />
      </Query>
    </DataSet>
    <DataSet Name="photos">
      <Fields>
        <Field Name="URL">
          <DataField>URL</DataField>
          <rd:TypeName>System.String</rd:TypeName>
        </Field>
        <Field Name="POSITION">
          <DataField>POSITION</DataField>
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

| Nom DataSet | Nom Champ                 | Définition                                                                      |
|:-----------:| ------------------------- | ------------------------------------------------------------------------------- |
| client      | ADR_COMPLEMENT            | Adresse /  Complément client                                                    |
| client      | ADR_NOVOIE                | Non utilisé                                                                     |
| client      | ADR_RUE                   | Adresse / Rue  client                                                           |
| client      | ADR_VILLE                 | Adresse /  Ville client                                                         |
| client      | ADR_CPOSTAL               | Adresse /  Code Postal client                                                   |
| client      | ADR_COUNTRY               | Adresse /  Pays client                                                          |
| client      | PHONE                     | Téléphone  client                                                               |
| client      | EMAIL                     | Email client                                                                    |
| fields      | adequation_besoin         | Champ personnalisé Koban (id du champ)                                          |
| fields      | pres_alternatives         | Champ personnalisé Koban (id du champ)                                          |
| fields      | entreprise_cible          | Champ personnalisé Koban (id du champ)                                          |
| fields      | fournisseurs_actuels      | Champ personnalisé Koban (id du champ)                                          |
| fields      | budget                    | Champ personnalisé Koban (id du champ)                                          |
| fields      | circuit_decision          | Champ personnalisé Koban (id du champ)                                          |
| fields      | remise_gadgets            | Champ personnalisé Koban (id du champ)                                          |
| fields      | ecoute_client             | Champ personnalisé Koban (id du champ)                                          |
| fields      | cadre_reglementaire       | Champ personnalisé Koban (id du champ)                                          |
| fields      | surfaces_traitement       | Champ personnalisé Koban (id du champ)                                          |
| fields      | materiel_maintenance      | Champ personnalisé Koban (id du champ)                                          |
| fields      | personnes_hygiene         | Champ personnalisé Koban (id du champ)                                          |
| fields      | processus_production      | Champ personnalisé Koban (id du champ)                                          |
| fields      | process_controle          | Champ personnalisé Koban (id du champ)                                          |
| fields      | plan_maintenance          | Champ personnalisé Koban (id du champ)                                          |
| fields      | frequence_usage           | Champ personnalisé Koban (id du champ)                                          |
| fields      | saisonnalite_activite     | Champ personnalisé Koban (id du champ)                                          |
| fields      | centres_interets_perso    | Champ personnalisé Koban (id du champ)                                          |
| fields      | presentation_indiv        | Champ personnalisé Koban (id du champ)                                          |
| fields      | points_attention          | Champ personnalisé Koban (id du champ)                                          |
| fields      | vocabulaire_adapte        | Champ personnalisé Koban (id du champ)                                          |
| fields      | clients_visites_nombre    | Champ personnalisé Koban (id du champ)                                          |
| fields      | clients_visites_potentiel | Champ personnalisé Koban (id du champ)                                          |
| fields      | visites_blanc_nombre      | Champ personnalisé Koban (id du champ)                                          |
| fields      | visites_blanc_potentiel   | Champ personnalisé Koban (id du champ)                                          |
| fields      | visites_rdv_nombre        | Champ personnalisé Koban (id du champ)                                          |
| fields      | visites_rdv_potentiel     | Champ personnalisé Koban (id du champ)                                          |
| fields      | prospects_nombre          | Champ personnalisé Koban (id du champ)                                          |
| fields      | prospects_potentiel       | Champ personnalisé Koban (id du champ)                                          |
| fields      | n_de_serie                | Champ personnalisé Koban (id du champ) de type  System string(caractères)       |
| fields      | sous_garantie             | Champ personnalisé Koban (id du champ) de type System.Boolean ( case à cocher)  |
| fields      | date_installation         | Champ personnalisé Koban (id du champ) de type System.DateTime (Format date)    |
| fields      | prix_ht                   | Champ personnalisé Koban (id du champ) de type System.Double (Format numérique) |
| photos      | URL                       | Url de l'image insérée sur fil de l'Objet dans Koban                            |
| photos      | POSITION                  | Position de l'image                                                             |
