## Writing entity classes
There are two base entity classes which need to be inherited for custom items:
Item used to present list items
{{
[ContentType](ContentType)
public class Item
{
    public virtual int Id { get; internal set; }
    public virtual string Title { get; set; }
    public virtual DateTime Created { get; internal set; }
    public virtual User Author { get; internal set; }
    public virtual DateTime Modified { get; internal set; }
    public virtual User Editor { get; internal set; }
    public virtual Version Version { get; internal set; }
    public virtual Guid Guid { get; internal set; }
}
}}
Document used to present files in document library
{{
[ContentType](ContentType)
public class Document : Item
{
    [NotField](NotField)
    public virtual string Name { get; set; }

    [NotField](NotField)
    public virtual byte[]() Content { get; set; }

    [NotField](NotField)
    public virtual long Size { get; internal set; }

    [NotField](NotField)
    public virtual string Icon { get; internal set; }

    [NotField](NotField)
    public virtual string Url { get; internal set; }

    [NotField](NotField)
    public virtual string Folder { get; set; }

    [NotField](NotField)
    public bool RenameIfExists { get; set; }
}
}}