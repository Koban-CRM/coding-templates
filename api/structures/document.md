# API Model Structure - Document

You can find here JSON structure for a document in the Koban API.

It is to be used for updates via the API and is also returned by the selection methods.

**Versions** : From August 2021

```
{
            "Label": "ACME - KOBAN - SPECIFICATIONS.pdf",
            "Third": {
                "Label": "ACME",
                "Extcode": null,
                "Guid": "57ecff7a0dc3610dc0c4df02",
                "DUpdated": 0,
                "Updated": "0001-01-01T00:00:00",
                "DCreated": 0,
                "Created": "0001-01-01T00:00:00"
            },
            "Deal": null,
            "Action": null,
            "Lead": null,
            "Contact": null,
            "Project": null,
            "Order": null,
            "CustomObject": null,
            "MediaUrl": "https://nocrmmedia.s3.eu-west-1.amazonaws.com/55018e75608776de640afda5_360---KOBAN---CONTRAT-APPORTEUR-AFFAIRE-2021---signe_20210322184618.pdf?AWSAccessKeyId=AKIAJ7E7TZUWJVQTCWNQ&Expires=1893452400&Signature=0ri64a6ms1xJAdmNEJrYVW0zGvo%3D",
            "Title": "ACME - KOBAN - SPECIFICATIONS.pdf",
            "Guid": "6058d7ea0dc3611a884ab894",
            "DUpdated": 1616438778.5379999,
            "Updated": "2021-03-22T18:46:18.538",
            "DCreated": 1616438778.5379999,
            "Created": "2021-03-22T18:46:18.538"
        }
```

| Property            | Comment                                                      | In POST methods                                         | In GET methods                               |
| ------------------- | ------------------------------------------------------------ | ------------------------------------------------------- | -------------------------------------------- |
| Label or Title      | Document title                                               | yes                                                     | yes                                          |
| MediaUrl            | Document absolute URL                                        | yes. Document added will be linked to this external URL | yes                                          |
| Guid                | Document Guid                                                | no                                                      | yes                                          |
| Updated or DUpdated | Document last updated date (and Timestamp format)            | no                                                      | yes                                          |
| Created or DCreated | Document creation date (and Timestamp format)                | no                                                      | yes                                          |
| Third               | Account linked, if exists                                    | yes. You must fill account guid or Extcode              | yes. Returns Account guid, Label and Extcode |
| Deal                | Deal linked, if exists                                       | yes. You must fill deal guid or Extcode                 | yes. Returns Deal guid and Extcode           |
| Action              | Action linked, if exists                                     | yes. You must fill action guid or Extcode               | yes. Returns Action guid                     |
| Lead                | Lead linked, if exists                                       | yes. You must fill lead guid or Extcode                 | yes. Returns Lead guid and Extcode           |
| Contact             | Contact linked, if exists                                    | yes. You must fill contact guid or Extcode              | yes. Returns Contact guid and Extcode        |
| Project             | Project linked, if exists                                    | no                                                      | yes. Returns Project guid                    |
| Order               | Order linked, if exists                                      | yes. You must fill order guid, Number or Extcode        | yes. Returns Order guid and Extcode          |
| CustomObject        | Custom object linked, if exists                              | yes. You must fill custom object guid or Extcode        | yes. Returns Custom object guid and Extcode  |
| Quote               | Quote linked, if exists                                      | yes. You must fill quote guid, Number or Extcode        | yes. Returns Quote guid and Extcode          |
| Invoice             | Invoice linked, if exists.<br />To retrieve invoice Koban PDF, you can use also /ncInvoice/GetPDF method | yes. You must fill invoice guid, Number or Extcode.     | yes. Returns Invoice guid and Extcode        |