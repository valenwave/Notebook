# LINQ to JSON
```cs
JArray array = new JArray();
array.Add("Manual text");
array.Add(new DateTime(2000, 5, 23));

JObject o = new JObject();
o["MyArray"] = array;

string json = o.ToString();
// {
//   "MyArray": [
//     "Manual text",
//     "2000-05-23T00:00:00"
//   ]
// }
```

# Using LINQ for JSON
```cs
JObject o = JObject.Parse(@"{
  'CPU': 'Intel',++
  'Drives': [
    'DVD read/writer',
    '500 gigabyte hard drive'
  ]
}");

string cpu = (string)o["CPU"];
// Intel

string firstDrive = (string)o["Drives"][0];
// DVD read/writer

IList<string> allDrives = o["Drives"].Select(t => (string)t).ToList();
// DVD read/writer
// 500 gigabyte hard drive
```
