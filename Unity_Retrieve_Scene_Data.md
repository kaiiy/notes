# How to Retrieve Data in a Scene

## 1. Retrieving GameObjects

### Setting in the Inspector

```csharp
public class Sample : MonoBehaviour
{
    [SerializeField] private GameObject _object;
    // public GameObject _object;
}
```

### Searching by GameObject Name

```csharp
GameObject obj = GameObject.Find("ObjectName");
```

### Searching by Attached Component

```csharp
GameObject obj = FindObjectOfType</*Component*/>().gameObject;
```

### Searching by Tag

```csharp
GameObject obj = GameObject.FindWithTag("Tag");
GameObject[] objs = GameObject.FindGameObjectsWithTag("Tag");
```

## 2. Retrieving Components

### Setting in the Inspector

```csharp
public class Sample : MonoBehaviour
{
    [SerializeField] private Example _object;
    // public Example _object;
}
```

### Using GetComponent

```csharp
var cmp = this.gameObject.GetComponent</*Component*/>();
var cmp = GameObject.Find("CUBE").GetComponent</*Component*/>();
```

### Retrieving from the Scene

```csharp
var cmp = FindObjectOfType</*Component*/>();
var cmp = FindObjectsOfType</*Component*/>();
```

