# Swift Example — Repository with Injected API

**Type:** Illustrative learning example.

```swift
protocol ProfileAPI {
    func profile(id: String) async throws -> ProfileDTO
}

protocol ProfileRepository {
    func profile(id: String) async throws -> Profile
}

struct DefaultProfileRepository: ProfileRepository {
    let api: ProfileAPI

    func profile(id: String) async throws -> Profile {
        let dto = try await api.profile(id: id)
        return Profile(id: dto.id, displayName: dto.name)
    }
}
```

## Why this boundary?
The feature/domain depends on a repository contract rather than transport details. Mapping prevents transport DTOs from automatically becoming domain models.

## Trade-off
For a tiny app this may be unnecessary indirection. Add the seam when testability, multiple data sources, mapping or change isolation justify it.
