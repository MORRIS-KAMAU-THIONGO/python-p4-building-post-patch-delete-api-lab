# TODO: Edit server/app.py to add POST, PATCH, and DELETE routes

## Information Gathered:
- Current server/app.py has GET routes for bakeries and baked goods
- Models are defined in server/models.py with Bakery and BakedGood classes
- Both models have to_dict() methods for JSON serialization
- Database uses SQLAlchemy with Flask
- Current routes use make_response(jsonify(data), status_code) pattern

## Plan:
Add three new routes to server/app.py:

1. **POST /baked_goods route**:
   - Handle form data (name, price, bakery_id)
   - Create new BakedGood instance
   - Add to database and commit
   - Return created baked good as JSON with 201 status

2. **PATCH /bakeries/<int:id> route**:
   - Handle form data for name update
   - Find bakery by ID
   - Update bakery name
   - Commit changes
   - Return updated bakery as JSON with 200 status

3. **DELETE /baked_goods/<int:id> route**:
   - Find baked good by ID
   - Delete from database
   - Commit changes
   - Return confirmation JSON message with 200 status

## Dependent Files to be edited:
- server/app.py - Add the three new routes

## Followup steps:
- Test the new routes to ensure they work correctly
- Verify database operations (create, update, delete) function properly

## COMPLETED:
✅ Added POST /baked_goods route with form data handling
✅ Added PATCH /bakeries/<int:id> route with name update functionality  
✅ Added DELETE /baked_goods/<int:id> route with confirmation message
✅ All routes follow existing code patterns and use proper HTTP status codes
✅ Database operations properly implemented with session management
