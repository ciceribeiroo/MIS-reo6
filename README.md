# Modelagem e Implementação de Software : REO 6

Repositório referente a *Atividade Prática 5* da matéria **Modelagem e Implementação de Software**. Vamos discutir um pouco da linguagem .NET.


#### O seguinte código representa a utilização de injeção de dependência em Asp .NET Core
`
private IRepository _repo;

private IFileManager _fileManager;

public HomeController(IRepository repo, IFileManager fileManager)
{

    _repo = repo;
    
    _fileManager = fileManager;
    
}
`
#### Outra funcionalidade muito usada em .NET é o uso de expressões ou métodos lambdas
`
public List<Post> GetAllPosts(string Category)
{

    Func<Post, bool> InCategory = (post) => { return post.Category.ToLower().Equals(Category.ToLower()); };
    return _ctx.Posts
    .Where(post => InCategory(post))
    .ToList();
}
`

Além do .NET instalados na sua máquina é necessáio ter:
 * Entity Framework Core
 * Banco de Dados SQL
 * Qualquer outro pacote NuGet necessário para seu projeto

Também é interessante ter
1. Git ou GitHub
2. Visual Studio Community 2019
