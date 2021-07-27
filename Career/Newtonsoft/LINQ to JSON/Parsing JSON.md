# Parsing a JSON Object from text
```cs
string json = @"{
  CPU: 'Intel',
  Drives: [
    'DVD read/writer',
    '500 gigabyte hard drive'
  ]
}";

JObject o = JObject.Parse(json);
```

# Parsing a JSON Array from text
```cs
string json = @"[
  'Small',
  'Medium',
  'Large'
]";

JArray a = JArray.Parse(json);
```

# Reading JSON from a file
```cs
using (StreamReader reader = File.OpenText(@"c:\person.json"))
{
    JObject o = (JObject)JToken.ReadFrom(new JsonTextReader(reader));
    // do stuff
}
```
