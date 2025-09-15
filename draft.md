# Commands

**`<>`** ─ Required  
**`[]`** ─ Optional

## Number

### `/number lookup`

Lookup a phone number.

> **Parameters**  
> `<number(s)>` : Phone numbers to lookup, separated by a comma.

### `/number report`

Report numbers to the carrier.

> **Parameters**  
> `<number(s)> ` : Phone numbers to report, separated by a comma.  
> `<type>      ` : The type of scam.  
> `[extra-info]` : Any additional information.

### `/number blocklist`

Add or remove phone numbers from the report block list.

> **Parameters**  
> `<todo>     ` : Add or remove...  
> `<number(s)>` : Phone numbers, separated by a comma.

## Template

### `/template set`

Add or update a report template.

> **Parameters**  
> `<type>` : Scam type.

> **Form Fields**  
> `<subj>` : Template subject (for emails.)  
> `<body>` : Template body.
>
> The following placeholders will be replaced:  
> `{num-e}` : External phone number(s) to report.  
> `{num-i}` : Internal phone number used to receive or make call.  
> `{time} ` : Timestamp of call.  
> `{extra}` : Extra info, should it be provided.

### `/template del`

Delete a report template.

> **Parameters**  
> `<type>` : Type of scam.

## Carrier

### `/carrier get`

Get stored carrier information.

> **Parameters**  
> `<carrier>` : The carrier.

### `/carrier set`

Update or add carrier information.

> **Parameters**  
> `<carrier>` : The carrier.

> **Form Fields**  
> `disp-name` : Display name.  
> `parent   ` : Parent carrier, if any.  
> `rep-email` : Report emails, separated by a comma.  
> `rep-form ` : Report form link.  
> `tz-offset` : Timezone offset. (Format:`+00:00`)  
> `req-info ` : Required info to make a report. (See Info Types)  
> `max-nums ` : Max numbers allowed per report.  
> `manual   ` : Manual reports only?  
> `note     ` : A note to display to the reporter.
>
> **Info Types**  
> `recording ` : Recording of call.  
> `timestamp ` : Timestamp of call.  
> `screenshot` : Screenshot of scam.  
> `num-did   ` : Internal number used to received call.  
> `num-cid   ` : Internal number used to make call.

## `/carrier del`

Delete stored carrier information.

> **Parameters**  
> `<carrier>` : The carrier.

## Query

### `/query reports`

Build a CSV report.

> **Parameters**  
> `<date:from> `  
> `<date:to>   `  
> `[carrier(s)]`
