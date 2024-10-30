# Code Style Guide

## Naming Conventions

### General Rules
- Use PascalCase for class names, public methods, and properties
- Use camelCase for private fields and local variables
- Use UPPER_SNAKE_CASE for constants
- Prefix interfaces with 'I' (e.g., `IWeapon`)
- Prefix private fields with '_' (e.g., `_health`)

### Unity-Specific
- Suffix MonoBehaviour classes with "Controller", "Manager", or "Behaviour" when appropriate
- Prefix SerializeField variables with descriptive tags:
  ```csharp
  [SerializeField] private float _moveSpeed;
  [SerializeField] private GameObject _projectilePrefab;
  ```

## Class Structure

### Organization
1. Serialized Fields
2. Public Properties
3. Private Fields
4. Unity Event Functions (Awake, Start, Update, etc.)
5. Public Methods
6. Private Methods

Example:

csharp
public class TowerController : MonoBehaviour
{
[SerializeField] private float attackRange;
[SerializeField] private float damage;
public bool IsActive { get; private set; }
private Enemy currentTarget;
private void Awake()
{
// Initialization
}
public void Attack(Enemy target)
{
// Attack logic
}
private void Fin
dTarget()
{
// Target finding logic
}
}

csharp
public class TowerController : MonoBehaviour
{
[SerializeField] private float attackRange;
[SerializeField] private float damage;
public bool IsActive { get; private set; }
private Enemy currentTarget;
private void Awake()
{
// Initialization
}
public void Attack(Enemy target)
{
// Attack logic
}
private void Fin
dTarget()
{
// Target finding logic
}
}


## Comments and Documentation

### Method Documentation
Use XML documentation for public methods:

csharp
/// <summary>
/// Deals damage to the specified target.
/// </summary>
/// <param name="target">The enemy to attack</param>
/// <param name="damage">Amount of damage to deal</param>
/// <returns>True if the target was destroyed</returns>
public bool DealDamage(Enemy target, float damage)


### Code Comments
- Use comments to explain "why", not "what"
- Keep comments concise and relevant
- Use TODO comments for future tasks:

csharp
// TODO: Implement damage multipliers for different enemy types


## Best Practices

### Unity-Specific
1. Cache component references in Awake:
csharp
private Transform transform;
private void Awake()
{
transform = transform;
}
2. Use [SerializeField] instead of public for inspector variables
3. Prefer ScriptableObjects for configuration data
4. Use events/actions for decoupled communication

### General
1. Follow Single Responsibility Principle
2. Keep methods short and focused
3. Avoid deep nesting
4. Use meaningful variable names
5. Implement interfaces for common behaviors

## Error Handling
1. Use null checks for references:
csharp
if (target == null)
{
Debug.LogWarning("Target is null");
return;
}
2. Validate parameters where appropriate
3. Use try-catch blocks sparingly and purposefully

## Performance Considerations
1. Cache component references
2. Avoid using Find methods in Update
3. Use object pooling for frequently spawned objects
4. Minimize garbage collection:
   - Cache vectors and other value types
   - Use StringBuilder for string operations
   - Pool lists and arrays when possible

## Version Control
1. Use meaningful commit messages
2. Keep commits focused and atomic
3. Comment complex code before committing

## Testing
1. Write testable code
2. Keep dependencies injectable
3. Use [SerializeField] for easier testing of private fields

