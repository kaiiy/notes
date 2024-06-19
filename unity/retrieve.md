# データの取得

## 1. GameObject の取得

### Inspector で設定

```cs
public class Sample : MonoBehaviour
{
    [SerializeField] private GameObject _object;
    // public GameObject _object;
}
```

### GameObject の名前で検索

```cs
GameObject obj = GameObject.Find("ObjectName");
```

### Component から GameObject を取得

```cs
GameObject obj = FindObjectOfType</*Component*/>().gameObject;
```

### Tag で検索

```cs
GameObject obj = GameObject.FindWithTag("Tag");
GameObject[] objs = GameObject.FindGameObjectsWithTag("Tag");
```

## 2. Component の取得

### Inspector で設定

```cs
public class Sample : MonoBehaviour
{
    [SerializeField] private Example _object;
    // public Example _object;
}
```

### GetComponent 

```cs
var component = this.gameObject.GetComponent</*Component*/>();
var component = GameObject.Find("CUBE").GetComponent</*Component*/>();
```

### Scene から取得

```cs
var component = FindObjectOfType</*Component*/>();
var component = FindObjectsOfType</*Component*/>();
```

